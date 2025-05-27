 ## 🤸🏼‍♂️ Process Stability & Variation analysis in Operations and Supply Chain using Microsoft Excel
 This respository presents a collection of practical case studies that explore **process stability**, **common cause variation**, and **special cause variation** using statistical analysis methods. The focus is on real-world operational processes such as manufacturing cycle times, supplier lead times, and customer service quality using Excel

---

## 🧑🏽‍🎤Process Stability Studies
| *Determine if the process is stable or not* | *Test for stability* |
| ------------------------------------------  |  ------------------  |
| 1. Measurement System Analysis (MSA)        | 1. Change should not be made to an unstable process|
| 2. Collection of data                       |                      |
| 3. Check for accuracy and validity          |                      |

- A process becomes unstable due to special cause of variation
- Multiple special causes of variation lead to instability
- A signal special cause leads to an out of control condition
---

## 🚣🏽 Causes of variation
Variation can be due to two type of causes:
### ** 1. Common Cause Variation **
- Includes many sources of variation within a process of inherent to it
- Contains a stable and repeatable distribution over time
- Contribute a state of statistical control where the output is predictable within a range
  - *Eg: Supplier lead time variability due to minor differences in shipment processing times; small delays due to traffic, weather, or loading queues, supplier's internal batching policy or shift schedules.*

### ** 2. Special Cause Variation **
- Includes factors external to and not always acting on the process
- Sporadic in nature
- Contribute to instability to a process output, which makes the process unpredictable
- May result in defects and have to be eliminated
- If identified, the point to the need for root cause analysis
   - *Eg: Sudden spike in supplier lead time due to port strike, supplier equipment breakdown, raw material shortage at the supplier's end, transportation failure*
 
## 🕶 Verifying Process stability and normality
For a stable process the same data used to determine stability can be used to calculate the process capability after normality is checked. Normality is the condition of a process that follows a normal distribution. 
- To address this, we need probability value (p-value), a statisitcal measurement used to validate hypothesis against observed data
- The lower the p-value, the greater the significance of the observed difference
- A p-value of 0.05 or lower is generally considered statistically significant
---

## 🦞 Case study 1: Production Line Cycle Time Stability

### 🏑 Objective
Analyze Cycle Time data across multiple shifts to determine if the production process is stable or impacted by specific causes 

### 🎲 Dataset
- Orders
- Standard resources
- Bottleneck Protection
- Cooling Time
- Preprocessing Time
- Production Capacity
- Production Time
- Transport Time

### 🧗‍♀️ Analysis
1. ** Key observations ** 
- Control chart (XṜ) to visualize shift level averages and range
- Detection of special cause variation on specific data points by considering top 51 line items through sampling method in excel
  - Most subgroups fall within control limits, including stable average time
  - Some occasional shifts suggest delays in specific production batches
  - Variability appears to increase in mid-batch runs - warranting further investigation into raw material consistency or machine calibration
  - Higher ranges in preprocessing transport stages suggest inconsistency
  - Specific outliers exceed control limits, pointing to potential breakdowns
  
2. ** Improvement areas **
- *TransportTime* fluctuations could be reduced by improving logistics scheduling
- *Preprocessing variability* suggests need for tighter operator SOPs
- Implement *real-time dashboards* to alert when Range exceeds predefined thresholds
