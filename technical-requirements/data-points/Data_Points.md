# Required Data Points for MDI Optimization System
*Analysis Date: 2024-11-10*

## Overview
This document outlines all potential data points identified for an MDI optimization system focused on systematic insulin adjustment through basal, ISF, and ICR refinement. While comprehensive, not all data points are required for initial implementation or basic functionality. Core requirements center on CGM data, insulin dosing, and essential user inputs, with enhanced data points providing improved accuracy and safety. Additional data points for system performance and user experience, while valuable for system refinement and validation, may be implemented in later phases. The following sections are organized by necessity, from critical core data to optional enhancement data, allowing for phased implementation while maintaining system safety and effectiveness.

## Initial Setup Data Provided by User
1. Confirmation and Acknowledgements
  - Diagnosis Confirmation date (Advise no use if < 12 months diagnosed, refer to health team)
  - Confirm all waivers including not fit for purpose and remind about medical advice at all levels
  - Confirm no Comorbidities
  - Explain bad data equals bad advice
  - Possible Knowledge Test To Allow Access
  - Explain this is a tool for assessing data only, any recommendations can be reviewed with medical professionals

2. Current Basal Regimen
  - Type of Basal Insulin used
  - Number of Daily Basal Injections
  - Dose at each period

3. Current Bolus Regimen
  - Type of Bolus Insulin used
  - Current ISF
  - Current ICR
  - Current pre / post meal bolus time

## Core CGM Data Points
1. Glucose Readings
   - Raw readings (5-minute intervals)
   - Timestamp for each reading
   - Data quality indicators
   - Gap information
   - Calibration status
   - Device metadata

2. Glucose Derived Metrics
   - Time in Range percentages
   - Rate of change calculations
   - Variability measures
   - Pattern confidence scores
   - Standard deviation
   - Coefficient of variation

## Insulin Data Points
1. Basal Insulin
   - Type of insulin
   - Dose amounts
   - Injection times
   - Duration of action
   - Split dose information
   - Historical changes

2. Bolus Insulin
   - Type of insulin
   - Dose amounts
   - Injection times
   - Purpose (meal/correction)
   - IOB calculations
   - Historical effectiveness

## Enhanced Data Points

1. User Input Data (Collected from CGM)
   - Meals
     - Timing
     - Carbohydrate content
     - Fat/protein content (optional)
     - Meal type/category (optional)
     - Pre/post meal tags
     - Skipped meal markers (optional)

2. Activity Data (Poss Steps / Heart Rate Integration)
   - Exercise sessions (Future iterations)
     - Type (aerobic/strength)
     - Duration
     - Intensity
     - Timing
     - Recovery periods
   
3. Sleep/Fasting Periods
   - Sleep start time (Can be assessed by Basal input, if user has Pre and Post bedtime basal.)
   - Wake time (Can be assessed by Basal input, if user has Pre and Post bedtime basal.)
   - Fasting periods (Can be assessed by lack of Carb input from user)
     - Start time
     - End time
     - Reason (intentional/unplanned)

4. Pattern Markers
   - Dawn phenomenon periods
   - Stress indicators (Poss heart rate, initiate prompt for user input eg, exercise / stress)
   - Illness markers
   - Temperature/weather (Minimal usefulness from experience)
   - Menstrual cycle (if applicable)
   - Travel/timezone changes

## Validation Data Points

1. Data Quality Metrics
   - CGM coverage percentage
   - Gap duration tracking
   - Sensor age
   - Calibration points
     - Reference BG readings
     - Timestamp
     - Sensor vs BG difference

2. Pattern Validation
   - Pattern occurrence count
   - Confidence scores
   - Variability measures
   - Confounding factors
   - Exception tracking

## Experimental Data Points (Require further investigation)

1. Basal Testing Data
   - Fasting Periods
     - Start/end timestamps
     - Last meal details
     - Starting glucose level
     - Hourly glucose trends
     - Success/failure markers
   - Overnight Periods
     - Pre-sleep glucose
     - Last meal timing
     - Overnight trends
     - Morning glucose
     - Pattern compliance score

2. ISF Testing Data
   - Correction Events
     - Starting glucose level
     - Correction dose
     - Time to effect
     - Glucose response curve
     - Target achievement
     - Confounding factors
   - Time-based Variations
     - Time of day
     - Response differences
     - Pattern consistency
     - Success rate

3. ICR Testing Data
   - Meal Tests
     - Pre-meal glucose
     - Carb amount
     - Insulin dose
     - Response curve
     - Peak time/value
     - Return to baseline
   - Ratio Validation
     - Time of day
     - Meal size variations
     - Success markers
     - Pattern reliability

## Safety Monitoring Data Points

1. Risk Indicators
   - Hypoglycemia
     - Event frequency
     - Severity levels
     - Recovery times
     - Treatment required
     - Contributing factors
   - Hyperglycemia
     - Duration
     - Severity
     - Correction response
     - Pattern correlation
     - Risk factors

2. Intervention Tracking
   - Treatment Actions
     - Type of intervention
     - Timing
     - Effectiveness
     - Side effects
     - Recovery pattern

## System Performance Data Points (Future Iterations)

1. Algorithm Performance
   - Recommendation Tracking
     - Type of suggestion
     - Implementation status
     - Success rate
     - User acceptance
     - Outcome measures
   - Pattern Recognition
     - Detection accuracy
     - False positive rate
     - False negative rate
     - Confidence levels
     - Pattern stability

2. Prediction Accuracy
   - Glucose Predictions
     - Forecast vs actual
     - Error rates
     - Time horizons
     - Confidence intervals
     - Contributing factors
   - Risk Predictions
     - Warning accuracy
     - Prevention success
     - False alarm rate
     - Miss rate
     - Risk factor correlation

## User Experience Data Points (Future Iterations)

1. Interaction Metrics
   - Data Entry
     - Completion rates
     - Time to input
     - Error frequency
     - Correction needs
     - User preferences
   - Alert Response
     - Response time
     - Action taken
     - Snooze usage
     - Dismissal patterns
     - Effectiveness

2. Compliance Tracking
   - Recommendation Adherence
     - Implementation rate
     - Modification patterns
     - Rejection reasons
     - Success correlation
     - User feedback
   - Testing Protocol Adherence
     - Completion rate
     - Quality measures
     - Problem areas
     - Success factors
     - Barrier identification

3. System Usage
   - Feature Utilization
     - Frequency of use
     - Feature preferences
     - Access patterns
     - Time spent
     - Navigation paths
   - Data Review
     - Review frequency
     - Depth of analysis
     - Action triggers
     - Understanding markers
     - Decision support usage