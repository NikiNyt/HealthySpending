# Technical Architecture & Rating System Logic

## 🏗️ System Overview
HealthySpending utilizes a Node.js architecture. The core innovation is the **User Meritocracy Engine**, which calculates user influence based on contributions.

## 🏆 Rating System Algorithm
The user rating determines the "weight" of a user's review.

### Scoring Formula
$$TotalPoints = (BasePoints) + (QuestMultipliers \times StreakBonus)$$

### User Tiers
1.  **Newcomer:** 0 - 100 points (Base feedback weight: 1.0)
2.  **Contributor:** 101 - 500 points (Base feedback weight: 1.2)
3.  **Elite Explorer / Verified Nutritionist:** 500+ points (Base feedback weight: 1.5)

*Note: Verified Nutritionists automatically start with a 1.5x weight on health-related validations.*

## 📂 Database Schema (Draft)
* **Users Table:** stores `ID`, `Role`, `CurrentPoints`, `ReputationScore`.
* **Locations Table:** stores `ShopData`, `HealthRating`, `VerifiedBy`.
* **Quests Table:** stores `DailyTaskID`, `PointValue`, `ExpirationDate`.
