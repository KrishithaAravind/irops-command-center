# Project Scope — IROPS Command Center ✈️📊

## 1) Intended user
This product is designed for an **Airline Operations Control / Network Operations Control (NOC)** team that monitors daily performance and manages disruptions (weather, congestion, staffing issues, aircraft rotation knock-on effects). Secondary users include station managers and performance reporting teams who need consistent KPI definitions.

## 2) Problem statement
Airline disruptions create cascading delays and operational costs. Teams often react after delays accumulate rather than seeing **early risk signals**. The goal is to provide a decision-support view that:
- surfaces **where/when disruption risk is rising**
- explains **what is driving the risk**
- recommends **actions operators can take immediately**

## 3) Decisions supported (what the dashboard is for)
The Command Center supports operational decisions such as:
- **Buffer management:** where to add turnaround or schedule buffer for high-risk flights/periods  
- **Resource triggers:** when to activate additional staffing/ground handling or contingency crew planning  
- **Prioritization:** which airports, routes, or time windows should be prioritized for monitoring and intervention  
- **Escalation rules:** which risk conditions should trigger review by ops leads (e.g., risk band “red” for an airport-hour)

## 4) Key outputs
The project delivers:
- **Disruption Risk Score:** probability/risk band for severe delay or late arrival by segment (airport × hour × weekday, and route where feasible)
- **Hotspot views:** heatmaps/maps showing concentrations of risk and severe delay rates
- **Driver analysis:** breakdown of likely contributors (time-of-day, congestion proxy, seasonality, carrier/route effects; plus weather if available)
- **Recommended actions panel (“Do this now”):** rule-based suggestions with reasons and estimated impact ranges

## 5) Success criteria (what “good” looks like)
The project is considered successful if it enables:
- **Earlier visibility:** risk hotspots identified **before** performance deteriorates (e.g., risk rising in upcoming time windows)
- **Actionability:** operators can select a hotspot and immediately see **recommended actions + rationale**
- **Consistent measurement:** KPI definitions are clear and reproducible (metric contracts)
- **Decision-ready insights:** the dashboard answers:
  1) What is happening?
  2) Where is it happening?
  3) Why is it happening?
  4) What should we do next?

## 6) Assumptions & boundaries
- The model and action panel provide **decision support**, not automated dispatch.
- Impact estimates may be scenario-based and depend on stated assumptions (documented in the repo).
- If detailed weather/crew/maintenance data is unavailable, the analysis will use proxies (e.g., congestion proxy from flight volumes).

## 7) Deliverables
- Cleaned dataset + KPI tables for BI
- Risk scoring notebook + evaluation results
- Power BI dashboard (4 pages) + screenshots
- 6-slide executive summary deck
