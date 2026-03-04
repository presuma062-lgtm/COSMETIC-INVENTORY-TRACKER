# Smart Cosmetic Inventory Tracker (Excel)

## Project Overview
A dynamic inventory management system built in Excel to track cosmetic product shelf life. It automatically calculates expiry dates and alerts the user when products are nearing their end-of-life.

## Key Features
* **Relational Database:** Uses `VLOOKUP` to pull shelf-life data from a 'Settings Library'.
* **Dynamic Date Math:** Utilizes `EDATE` to calculate exact expiry dates based on opening dates.
* **3-Color Alert System:** * **RED:** Expired
    * **YELLOW:** Expiring within 30 days
    * **GREEN:** Active/Safe to use
* **Automated Status Logic:** A nested `IF` statement that updates daily using the `TODAY()` function.

## Formulas Used
* `=VLOOKUP(B3, 'Settings Library'!$A$3:$B$7, 2, FALSE)`
* `=IF(H3 < TODAY(), "EXPIRED", IF(H3 <= EDATE(TODAY(), 1), "EXPIRING SOON", "ACTIVE"))`
