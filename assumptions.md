# Key Business Assumptions – Paris Transit Database Design

This document outlines the core business assumptions made during the database design process.  
These assumptions ensure the model aligns with operational requirements while maintaining data integrity.

---

## Training
- Training modules last **1–5 days**.  
- Training validity is capped at **10 months**.  
- Drivers may complete multiple training modules; historical records are retained.  

---

## Vehicles
- Each vehicle has **fewer than 100 seats**.  
- Odometer readings are restricted to **below 100,000**.  

---

## Drivers
- Driver–Language is a **many-to-many relationship**, managed through a bridge table.  
- Driver Security Level can only be:  
  - **FULL (F)** or **RESTRICTED (R)**  
  - Default value = Restricted  
- Driver Suspension Status can only be:  
  - **Suspended (S)** or **Not Suspended (N)**  
  - Default value = Not Suspended  

---

## Trips
- `trip_pickup_actual_datetime` and `trip_dropoff_actual_datetime` are optional fields, since forms may not always capture them.  

---

## Officials
- Officials may or may not have team members assigned (team member ID is optional).  

---

## Population & Scale
- The model assumes the supported population is **below 1.5 billion**.  
- This ensures scalability while remaining realistic for the operational scope.  

---

These assumptions were applied to guide entity design, enforce constraints, and ensure the database remains consistent with business rules.
