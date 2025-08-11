# Electric Vehicle (EV) Kinematic Dataset

## Overview

This comprehensive dataset contains **197.5 hours** of high-resolution driving data from **25 drivers** across **9 electric vehicle models**, specifically designed to investigate EV car-following behaviors and regenerative braking dynamics. The dataset addresses the critical gap in understanding how electric vehicles' unique kinematic characteristics impact traffic flow patterns.



## Download Source (Partially public)

*EV*

[KIA Niro](https://www.dropbox.com/scl/fo/fmw01x88h2a6cg79f3vq9/AHolXiHiZh0ZNEi0m7Gu1Bo?rlkey=1mjk80bcwmg57frwl7a6pdkud&st=rigc60ma&dl=0)



*ICEV Comparision*

[Toyota Camry 2021](https://www.dropbox.com/scl/fo/ho6u96pauyvjpgodlhhlr/AEZya3nv726la8PAnDHUmiY?rlkey=zmf1umkn4o6kty9alitq9vpu6&st=zeh41z1t&dl=0)



## Dataset Composition

### Data Sources

**Primary Collection (144.9 hours)**

- **Location**: Tampa International Airport area, Florida
- **Duration**: June 2024 - Present
- **Collection Method**: Professional vehicle logging tools + dash cameras
- **Vehicles**: 6 EV models (Tesla Model 3/X/Y, Kia Niro/EV6, Hyundai Ioniq 5, Ford Mach-E)

**Community Data (52.6 hours)**

- **Source**: Comma Community open dataset
- **Coverage**: Global driving data
- **Additional Models**: Expanded to 9 total EV models
- **Contributors**: 21 additional drivers worldwide

### Vehicle Models Included

| Manufacturer  | Models                    | Data Hours  |
| ------------- | ------------------------- | ----------- |
| **Tesla**     | Model 3, Model X, Model Y | ~80 hours   |
| **Hyundai**   | Ioniq 5                   | ~35 hours   |
| **Kia**       | Niro EV, EV6              | ~40 hours   |
| **Ford**      | Mach-E                    | ~25 hours   |
| **Chevrolet** | Bolt                      | ~17.5 hours |

### Driver Demographics

- **Experience Range**: < 1 week to > 10 years
- **EV Experience**: Novice to highly experienced EV drivers
- **Driving Styles**: Timid, normal, and aggressive drivers
- **Age Range**: Beginner drivers to experienced professionals

## Data Characteristics

### High-Resolution Metrics

- **Sampling Rate**: 100Hz for critical parameters
- **Temporal Coverage**: > 10,000 miles of driving
- **Traffic Conditions**: Free-flow and congested scenarios

### Recorded Parameters

**Vehicle Dynamics**

- Speed (m/s)
- Acceleration/Deceleration (m/s²)
- Pedal position (%)
- Brake status/position
- Regenerative braking level

**Environmental Context**

- Following distance (m)
- Leading vehicle behavior
- Traffic density conditions
- Road type and geometry

**EV-Specific Features**

- Regenerative braking intensity (1-4 m/s²)
- One-pedal driving mode status
- Motor torque characteristics
- Energy recovery data

## Key EV Kinematic Findings

### Distinctive Characteristics Captured

1. **High Pedal Sensitivity**
   - Less than 1/5 of pedal travel covers full propulsion to peak regenerative braking
   - Immediate regenerative engagement upon throttle release
2. **Constant Acceleration/Deceleration Profiles**
   - Nearly constant peak acceleration over broad speed ranges
   - Fixed regenerative deceleration (0.1-0.3g) based on user settings
3. **Elimination of Coasting Phase**
   - Instantaneous transition from acceleration to regenerative braking
   - No inertia-driven coasting buffer unlike ICEVs
4. **Transition Patterns**
   - Brief constant-speed phases between acceleration changes
   - Jerk-limited transitions for comfort and safety

## Dataset Structure

```
EV_Dataset/
├── HONDA_ACCORD/          # Honda vehicle data
├── Hyundai_IONIQ_5/       # Hyundai Ioniq 5 data
├── KiaNiro/               # Kia Niro EV data
│   ├── [driver_id]/
│   │   ├── [session_id]/
│   │   │   ├── data.csv           # High-frequency vehicle data
│   │   │   ├── reset/             # Processed data
│   │   │   ├── results/           # Analysis results
│   │   │   └── video/             # Dash cam footage
├── KIA_EV6/               # Kia EV6 data
├── MACH-E/                # Ford Mach-E data
├── RAV4/                  # Reference ICEV data
├── TESLA_AP3_MODEL3/      # Tesla Model 3 (AP3) data
├── TESLA_MODEL3/          # Tesla Model 3 data
└── TOYOTA_CAMRY_2021/     # Reference ICEV data
```

## Data Quality & Validation

- **Accuracy**: Validated against dynamometer measurements
- **Completeness**: Comprehensive car-following scenarios captured
- **Consistency**: Standardized logging protocols across all vehicles
- **Ground Truth**: Dash cam validation for leading vehicle behavior

## Applications

### Research Areas

- **Traffic Flow Modeling**: EV-specific car-following behavior
- **Capacity Analysis**: Impact of regenerative braking on road capacity
- **Control Systems**: Adaptive cruise control optimization
- **Energy Studies**: Regenerative braking efficiency analysis
- **Safety Research**: EV-ICEV interaction dynamics

### Use Cases

- Microscopic traffic simulation calibration
- EV-aware traffic signal optimization
- Highway capacity assessment
- Driver behavior analysis
- Autonomous vehicle development

## Data Access

**Repository**: https://github.com/OpenLKA/EV_Dataset

**File Formats**:

- `.csv` - Time-series vehicle data
- `.mp4/.avi` - Dash cam video footage
- `.json` - Metadata and session information

## Contact

- **Principal Investigator**: Dr. Hao Zhou, University of South Florida
- **Email**: haozhou1@usf.edu
- **Dataset Contributors**: Yuhang Wang (yuhangw@usf.edu)

## License

This dataset is released under an open-source license to facilitate research in electric vehicle traffic dynamics and sustainable transportation systems.

## Acknowledgments

- University of South Florida Department of Civil and Environmental Engineering
- Comma Community for open-source contributions
- Tampa International Airport for data collection support
- All volunteer drivers who contributed to this dataset

------

*This dataset represents the first comprehensive, multi-vehicle, multi-driver collection specifically designed to understand electric vehicle car-following dynamics and their impact on traffic flow.*
