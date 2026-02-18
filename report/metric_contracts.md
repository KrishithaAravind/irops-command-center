# Metric Contracts — IROPS Command Center

## North Star
**On-Time Arrival Rate (OTA):** % of flights arriving <= 15 minutes late.
- **Numerator:** flights with arrival_delay_minutes <= 15
- **Denominator:** all completed flights (exclude cancelled/diverted unless stated)

## Supporting Metrics
1) **Average Arrival Delay (AAD):** mean(arrival_delay_minutes) for completed flights  
2) **Severe Delay Rate (SDR):** % flights with arrival_delay_minutes >= 60  
3) **Cancellation Rate (CR):** cancelled / scheduled  
4) **Diversion Rate (DR):** diverted / scheduled

## Segments (must support)
- Origin airport
- Destination airport
- Route (origin-destination)
- Day of week
- Hour of departure (binned)
- Month / season

## Definitions / edge cases
- Cancelled flights: excluded from delay metrics; included in CR
- Diverted flights: excluded from delay metrics; included in DR
- Timezone handling: treat timestamps as local airport time if available
