# Aviation Accident Analysis

## Overview
This project analyzes aviation accident data from 1948 to 2023 to identify aircraft makes and models associated with lower risks of:

* Fatal injuries
* Serious injuries
* Aircraft destruction

The goal is to provide data-driven recommendations for an airline insurer to help them assess aircraft safety across manufacturers, models, and operational conditions.

The analysis focuses on professional, commercially built airplanes that could still be in active use today.

## Objectives

The analysis aims to:

Identify the safest aircraft makes and models
Compare the safety between small (≤20 passengers) and large (>20 passengers) aircraft
Quantify:
Fatal injury rate
Serious injury rate
Aircraft destruction probability
Determine key risk factors affecting aviation safety:
Weather conditions
Phase of flight
Engine configuration
Ensure statistically reliable results using minimum sample thresholds

## Dataset
Source: Aviation accident records (1948–2023)
Key fields include:
Aircraft Make & Model
Aircraft Category
Event Date
Injury counts (fatal, serious, minor, uninjured)
Aircraft damage status
Weather conditions
Flight phase
Engine type and count

## Data Cleaning & Preparation

Key preprocessing steps included:

* Filtering
Keep only Airplanes
Excluded amateur-built aircraft
Restricted analysis to events from 1983 onwards
* Missing Data Handling
Injury fields filled with 0 where appropriate
Critical fields (make, model, damage) with missing values removed
* Standardization
Normalized text fields (Make, Model, Weather, Engine Type, etc.)
Unified categorical labels for consistency
* Feature Engineering

Created key safety metrics:

fatal.rate = fatal injuries / total passengers
serious.rate = serious injuries / total passengers
injury.risk = fatal + serious injury rate
destruction = binary aircraft loss indicator
aircraft.id = Make + Model identifier

## Analysis Approach
1. Aircraft Segmentation

Aircraft were divided into:

Small aircraft: ≤ 20 passengers
Large aircraft: > 20 passengers
2. Safety Evaluation Metrics

Aircraft safety was assessed using:

Mean fatal injury rate
Mean serious injury rate
Aircraft destruction probability

To ensure reliability:

Only aircraft with ≥ 30 recorded incidents were included in model-level comparisons
3. Manufacturer Analysis

Manufacturers (Makes) were evaluated by:

Average injury risk per Make
Separate ranking for small vs large aircraft

The top 15 safest manufacturers were identified for each category.

## Key Insights
* Aircraft Size Matters
Small aircraft show higher variability in safety outcomes
Large aircraft generally demonstrate lower fatality rates per passenger
* Environmental Factors
Weather conditions significantly influence accident severity
Poor visibility conditions increase the likelihood of fatal and serious injuries
  * Flight Phase Risk
Takeoff and landing phases are consistently the most dangerous stages of flight
* Manufacturer Variation
Safety performance varies significantly across manufacturers
Some manufacturers consistently show lower injury and destruction rates
  * Outputs

The project produces:

Ranked list of safest aircraft makes and models
Comparative analysis of small vs large aircraft safety
Visualizations of:
Injury risk distribution
Destruction probability
Manufacturer comparisons
Risk factor analysis across environmental and operational conditions

## Technologies Used
Python

Pandas

NumPy

Matplotlib

Seaborn
