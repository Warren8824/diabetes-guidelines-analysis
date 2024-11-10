# Required Calculations for MDI Optimization System
*Analysis Date: 2024-11-09*

## Overview
This document outlines the calculations required for MDI optimization, structured in order of necessity for system functionality. Core calculations focus on essential basal, ISF, and ICR optimizations, with additional calculations providing enhanced accuracy and safety features. The structure allows for modular, iterative development while maintaining system integrity. Calculations are organized from critical core functions to optional enhancements, supporting phased implementation.

## Core Glucose Analysis Calculations
1. Basic Metrics
   - Time in Range (TIR)
     - Percentage within 3.9-10.0 mmol/L
     - Percentage below 3.9 mmol/L (Hypoglycemic)
     - Percentage below 3.0 mmol/L (Severely Hypoglycemic)
     - Percentage above 10.0 mmol/L (Hyperglycemic)
     - Percentage above 13.9 mmol/L (Possible DKA)
     - Percentage within User Defined Range - User range has to be within 3.9 - 10.0 mmol/L (Current guidelines).
     - percentage below Use Defined Range
     - percentage above User Defined Range
   - Glucose Descriptive Statistics
     - Estimated HbA1c (mmol/mol)
     - Estimated HbA1c (%)
     - 7 day moving average (Mean BG)
     - 30 day moving average (Mean BG)
     - 90 day moving average (Mean BG)
   - Glucose Variability
     - Standard deviation
     - Coefficient of variation
     - Rate of change
     - GVI

2. Pattern Detection
   - Fasting Period Analysis
     - Average glucose levels
     - Rate of change during fasting
     - Pattern consistency score
     - Variability during fasting
   - Overnight Patterns
     - Stability scores
     - Dawn phenomenon detection
     - Rise/fall rates
     - Pattern frequency

## Data Quality Metrics
- **Reliability Calculations**
  - CGM Data Quality
    - Data completeness percentage
    - Gap frequency analysis
    - Calibration accuracy score (Future Iterations)
    - calibration frequency score (Future Iterations)
    - Noise level assessment
    - Suspected missed inputs Carbs / Insulin (Future Iterations)
  
- **Input Validation**
  - Data Verification
    - Input consistency checking
    - Time stamp validation
    - Value range verification
    - Logical sequence confirmation
 
## Insulin Optimization Calculations

### 1. Basal Optimization (Primary Focus)
- **Fasting Analysis**
  - Base Rate Calculation
    - Average glucose change during validated fasting periods
    - Pattern consistency scoring
    - Standard deviation of fasting periods
    - Validation thresholds for stable periods
  
- **Overnight Assessment**
  - Stability Calculation
    - Hour-by-hour glucose delta
    - Dawn phenomenon impact measurement
    - Pattern repeatability score
    - Variability assessment

- **Adjustment Recommendations**
  - Change Magnitude
    - Percentage change needed (max 10-20%)
    - Time-block specific adjustments (Future Iterations)
    - Confidence scoring for recommendations
    - Impact prediction (Future Iterations)

### 2. ISF Optimization (Secondary Focus)
- **Correction Factor Analysis**
  - Basic ISF Calculation
    - Glucose change per unit insulin
    - Time to effect measurement
    - Duration of action tracking
    - Response curve analysis
  
- **Time-Based Variations**
  - Period Specific ISF
    - Morning resistance calculation
    - Time-block effectiveness (Future Iterations, morning/afternoon/evening)
    - Pattern consistency scoring
    - Adjustment recommendations

### 3. ICR Optimization (Tertiary Focus)
- **Ratio Calculations**
  - Basic ICR Determination
    - Glucose impact per carb unit (10g)
    - Response curve analysis
    - Peak time calculation
    - Duration of effect

### 4. Meal Bolus Timing ( Possible Future Direction)

### 5. Dawn Phenomenon Pre-emptive Bolus (Possible Future Direction)

### 6. Stomach Motility Assessment - Gastroparesis Risk Assessment (Possible Future Direction)

### 7. Individual Meal ICR Calculations - Time based & Composition based (Possible Future Direction)

## Safety Validation Calculations

### 1. Risk Assessment
- **Hypoglycemia Prevention**
  - Risk Scoring
    - Current trajectory analysis
    - IOB impact calculation
    - Activity factor assessment
    - Historical pattern matching

- **DKA Prevention**
  - Risk Scoring
    - Glucose Level
    - 24 hour rolling TAR
    - COB impact calculation

- **Target Distance from Current Levels**
  - Ensure steady improvement of glucose levels
  - implement strict regimen adjustment limits to ensure gradual improvements
  - Avoid rapid drops in HbA1c over short periods of time (**Requires further research**)

- **Pattern Safety**
  - Validation Metrics
    - Data completeness percentage
    - Pattern confidence scoring
    - Variation threshold checking
    - Exception identification

### 2. Recommendation Validation
- **Change Safety**
  - Adjustment Validation
    - Maximum change verification
    - Cumulative impact assessment
    - Recovery pattern prediction
    - Risk factor evaluation

## System Performance Calculations

### 1. Recommendation Accuracy
- **Success Metrics**
  - Outcome Analysis
    - Recommendation success rate
    - Target achievement percentage
    - Time to goal calculation
    - Stability improvement measurement
  
- **Pattern Recognition Performance**
  - Accuracy Metrics
    - True positive rate
    - False positive rate
    - Pattern reliability score
    - Prediction accuracy percentage

## Enhanced Calculations (Future Iterations)

### 1. Pattern Enhancement
- **Advanced Pattern Detection**
  - Multi-factor Analysis
    - Exercise impact quantification
    - Stress/illness effect measurement
    - Weather/temperature correlation
    - Time zone adjustment impact
  
- **Meal Impact Analysis**
  - Complex Meal Calculations
    - Fat/protein impact measurement
    - Extended absorption patterns
    - Meal size correlation
    - Timing impact quantification

### 2. Predictive Calculations
- **Glucose Prediction**
  - Trend Analysis
    - Short-term projection (30 min)
    - Medium-term projection (2 hours)
    - Confidence interval calculation
    - Risk probability assessment

- **Pattern Prediction**
  - Behavioral Impact
    - Activity influence prediction
    - Meal timing impact
    - Sleep pattern effect
    - Routine change impact

## Quality Assurance Metrics

### 1. User Compliance
- **Adherence Calculations**
  - Protocol Following
    - Testing completion rate
    - Data entry timeliness
    - Required input completion
    - Protocol deviation tracking
  
- **Interaction Analysis**
  - Usage Patterns
    - Feature utilization rate
    - Response time calculations
    - Alert acknowledgment rate
    - Data review frequency

### 2. System Effectiveness
- **Optimization Progress**
  - Goal Achievement
    - Time in range metrics vs Assessment stage
    - Time user defined in range metrics vs Assessment stage
    - Optimised regimen vs Original regimen
    - Stability improvement rate (statistical measure of variability, rolling averages etc)
    - Complication reduction (Hypo Events and > 13.9 mmol/L events)
    - Quality of life impact (Undefined)
  
- **Long-term Success**
  - Outcome Tracking
    - Sustained improvement measures
    - Regression analysis
    - Adaptation requirements
    - Maintenance needs