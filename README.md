 ## 🤸🏼‍♂️ Process Stability & Variation analysis in Manufacturing operations using Six Sigma methodology in Microsoft Excel
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
- Detection of special cause variation at specific data points by considering top 51 line items through **sampling** technique (top 100 data points) in Excel
  - Most subgroups fall within control limits, including stable average time
  - Some occasional shifts suggest delays in specific production batches
  - Higher ranges in preprocessing transport stages suggest inconsistency
  - Specific outliers exceed control limits, pointing to potential breakdowns
 - *Performed T.Test on Mean (X-bar)* to compare the cycle time and machine efficiency evaluation || The observed p-value for the sample dataset of 100 line items are statisically significant as the value is lesser than 0.05
 - *Performed F.Test on Range (R)* to monitor process stability and machine variability || The observed p-value for the sample dataset of 100 line items are statisically significant as the value is lesser than 0.05
  
2. ** Improvement areas **
- *TransportTime* fluctuations could be reduced by improving logistics scheduling
- *Preprocessing variability* suggests need for tighter operator SOPs
- Implement *real-time dashboards* to alert when Range exceeds predefined thresholds

## 🧌 Case study 2: OTIF (On-Time In-Full) Delivery analysis using X-R control chart

### 🏃‍♂️‍➡️ Objective
Evaluate the stability of OTIF delivery performance across customer order lines to:
- Identify process consistency
- Detect abnormal delivery trends
- Enable continuous improvement in supply chain execution

### 🪢 Dataset
- Order Qty
- Delivery Qty
- OTIF flag ('1 = Delivered on Time and In Full', '0 = Not OTIF')
- Promise Date
- Forward Operating Location (FOL) date/Delivery confirmation date

### 🏌🏻 Analysis
1. ** Key observations **
- Control chart (XṜ) to visualize OTIF averages ranging by weekly delivery period
- Detection of special cause variation (OTIF underperformed) at specific data points by considering top 100 line items through **sampling** technique in Excel
   - Outliers are detected which are caused by system errors, supplier issues, or transportation strikes

 ---
 
## 🧳 Repository structure
Manufacturing_sample dataset.xlsm
  - Standard resources
  - COLDs

---

## 🤌🏻 Excel functionalities used
1. Pivot tables & Pivot Charts
2. IF() conditional statement
3. IFAND() function
4. Line chart
5. RANDBETWEEN() function
6. RAND() function
7. AVERAGE() function
8. T.Test() for Mean value array
9. F.Test() for Range value array

---

## 🏋🏻 Requirements
- Microsoft Excel 2016 or later
- Basic understanding of OTIF, Six Sigma fundamentals, Manufacturing operations
