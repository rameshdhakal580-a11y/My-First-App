## 🚖 Pricing Engine Specification (Finalized May 2026)

This project uses a "Balanced Marketplace" algorithm to handle taxi and ride-hailing fares in Pokhara, specifically adjusted for the current fuel price of **Rs. 217/L**.

### 1. Fare Constants
| Variable | Value | Description |
| :--- | :--- | :--- |
| **Flag Down** | Rs. 80.00 | Initial starting fee for every ride. |
| **Day Pulse** | Rs. 13.00 | Rate per 200 meters (6 AM - 9 PM). |
| **Night Pulse** | Rs. 15.50 | Rate per 200 meters (9 PM - 6 AM). |
| **Gov. Fees** | 3.0% | Includes 2% Provincial & 1% Accident Funds. |

### 2. Pricing Logic (Formula)
Total Fare = (Flag Down + ((Distance_in_Meters / 200) * Pulse_Rate)) * 1.03

### 3. Target Benchmarks (4 km Trip)
*   **Daytime:** ~Rs. 350.00
*   **Night-time:** ~Rs. 400.00 (Compensation for "sleep-killing" shifts).
