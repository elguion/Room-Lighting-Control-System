# Intelligent Room Lighting Control System
Phase A
### Concept & Technology Development

---

## 📋 Project Overview

**Project Name**: Adaptive Intelligent Lighting Control System (AILCS)

**Mission Statement**: Design and implement an intelligent lighting control system that optimizes energy consumption, enhances occupant comfort, and adapts to environmental conditions through autonomous sensor-based control.

**Project Duration**: 12 weeks (from Pre-Phase A to Phase F)

**Budget Allocation**: Educational project scale (~$500 implementation budget)

---

## 🎯 Phase A: Concept & Technology Development

### A.1 STAKEHOLDER ANALYSIS

#### Primary Stakeholders:
1. **End Users (Room Occupants)**
   - Need: Comfortable lighting conditions
   - Expectation: Minimal manual intervention
   - Priority: Visual comfort and convenience

2. **Facility Management**
   - Need: Reduced energy consumption
   - Expectation: 30-40% energy savings
   - Priority: Cost efficiency and sustainability

3. **Safety & Compliance**
   - Need: Adequate illumination for safety
   - Expectation: Meet building code requirements
   - Priority: Regulatory compliance

4. **Maintenance Personnel**
   - Need: Reliable, maintainable system
   - Expectation: Easy troubleshooting
   - Priority: Low maintenance overhead

#### Secondary Stakeholders:
- Environmental organizations (carbon footprint reduction)
- Electrical utilities (demand management)
- Building owners (property value enhancement)

---

## 📊 SYSTEM REQUIREMENTS SPECIFICATION

### 1. MISSION REQUIREMENTS (Level 0)

**MR-001**: The system SHALL automatically control room lighting based on occupancy and ambient light conditions.

**MR-002**: The system SHALL achieve minimum 30% energy savings compared to conventional always-on lighting.

**MR-003**: The system SHALL provide adequate illumination levels per IESNA standards (300-500 lux for office spaces).

**MR-004**: The system SHALL operate continuously with 99.5% availability over one year.

**MR-005**: The system SHALL respond to environmental changes within 2 seconds.

---

### 2. FUNCTIONAL REQUIREMENTS (Level 1)

#### 2.1 Occupancy Detection
**FR-001**: The system SHALL detect human presence within 5 meters range with 95% accuracy.

**FR-002**: The system SHALL distinguish between motion and static occupancy.

**FR-003**: The system SHALL implement a configurable timeout period (default: 5 minutes) before turning off lights after last detected motion.

**FR-004**: The system SHALL maintain a log of occupancy events with timestamps.

#### 2.2 Ambient Light Sensing
**FR-005**: The system SHALL measure ambient light levels with ±10% accuracy in the range of 0-10,000 lux.

**FR-006**: The system SHALL sample ambient light levels at minimum 1 Hz frequency.

**FR-007**: The system SHALL compensate for artificial light contribution in ambient measurements.

**FR-008**: The system SHALL adapt to gradual changes in natural light (sunrise/sunset transitions).

#### 2.3 Lighting Control
**FR-009**: The system SHALL support dimming control from 0% to 100% in minimum 1% increments.

**FR-010**: The system SHALL implement smooth transitions (fade in/out) over 1-2 second periods.

**FR-011**: The system SHALL maintain target illumination levels within ±50 lux tolerance.

**FR-012**: The system SHALL support manual override capability with automatic resumption after 2 hours.

#### 2.4 Control Logic
**FR-013**: The system SHALL implement closed-loop feedback control to maintain target illumination.

**FR-014**: The system SHALL use predictive algorithms to anticipate lighting needs based on historical patterns.

**FR-015**: The system SHALL prioritize natural light utilization before artificial lighting.

**FR-016**: The system SHALL operate in multiple modes: Auto, Manual, Energy-Saver, and Presentation.

#### 2.5 Energy Management
**FR-017**: The system SHALL monitor and report real-time power consumption.

**FR-018**: The system SHALL calculate and display cumulative energy savings.

**FR-019**: The system SHALL implement load shedding during peak demand periods (if configured).

**FR-020**: The system SHALL optimize lighting schedules based on usage patterns.

#### 2.6 User Interface
**FR-021**: The system SHALL provide a physical interface with minimum 3 buttons (On/Off, Mode, Brightness).

**FR-022**: The system SHALL provide visual feedback via LED indicators for system status.

**FR-023**: The system SHALL provide a web-based dashboard for monitoring and configuration.

**FR-024**: The system SHALL support remote access for authorized users.

---

### 3. PERFORMANCE REQUIREMENTS (Level 2)

#### 3.1 Response Time
**PR-001**: Occupancy detection to light activation: ≤ 500ms

**PR-002**: Ambient light change to output adjustment: ≤ 2 seconds

**PR-003**: Manual override response: ≤ 200ms

**PR-004**: Control loop update rate: ≥ 10 Hz

#### 3.2 Accuracy & Precision
**PR-005**: Illumination level accuracy: ±50 lux

**PR-006**: Occupancy detection accuracy: ≥ 95%

**PR-007**: False positive rate (lighting when unoccupied): < 2%

**PR-008**: False negative rate (not lighting when occupied): < 0.5%

#### 3.3 Energy Efficiency
**PR-009**: System idle power consumption: ≤ 2W

**PR-010**: Control system efficiency: ≥ 85%

**PR-011**: Standby power: ≤ 0.5W

**PR-012**: Energy savings target: 30-40% vs. baseline

#### 3.4 Reliability & Availability
**PR-013**: Mean Time Between Failures (MTBF): ≥ 50,000 hours

**PR-014**: System availability: ≥ 99.5% annually

**PR-015**: Sensor lifespan: ≥ 5 years

**PR-016**: Maximum allowable downtime: 2 hours/month

---

### 4. INTERFACE REQUIREMENTS (Level 2)

#### 4.1 Electrical Interfaces
**IR-001**: Input voltage: 100-240VAC, 50/60Hz

**IR-002**: Control voltage: 5VDC for sensors, 12VDC for actuators

**IR-003**: Output: PWM signal 0-10V or DALI protocol for dimmable drivers

**IR-004**: Maximum load capacity: 500W per channel

#### 4.2 Communication Interfaces
**IR-005**: Sensor communication: I2C or analog (0-5V)

**IR-006**: Network connectivity: WiFi 802.11 b/g/n

**IR-007**: Web interface: HTTPS on port 443

**IR-008**: API: RESTful JSON over HTTP

#### 4.3 Physical Interfaces
**IR-009**: Mounting: Standard electrical box compatible

**IR-010**: User controls: Push buttons, capacitive touch optional

**IR-011**: Indicators: RGB LED status display

**IR-012**: Environmental: IP20 rating minimum

---

### 5. ENVIRONMENTAL REQUIREMENTS

#### 5.1 Operating Environment
**ER-001**: Operating temperature: 0°C to 50°C

**ER-002**: Storage temperature: -20°C to 70°C

**ER-003**: Relative humidity: 10% to 90% non-condensing

**ER-004**: Altitude: 0 to 3000m above sea level

#### 5.2 Electromagnetic Compatibility
**ER-005**: EMI compliance: FCC Part 15 Class B

**ER-006**: ESD immunity: ±4kV contact, ±8kV air discharge

**ER-007**: Power line transients: Per IEC 61000-4-4

#### 5.3 Safety & Standards
**ER-008**: Electrical safety: UL/CE certified components

**ER-009**: Fire rating: UL94 V-0 materials

**ER-010**: Photobiological safety: IEC 62471 compliance

---

### 6. DESIGN CONSTRAINTS

**DC-001**: Total system cost: ≤ $500 for prototype

**DC-002**: Microcontroller: Arduino-compatible or ESP32 platform

**DC-003**: Installation: Retrofit-compatible with existing wiring

**DC-004**: Physical size: Fit within standard 2-gang electrical box

**DC-005**: Development time: 12 weeks from concept to deployment

**DC-006**: Programming language: C/C++ for embedded, Python for analytics

**DC-007**: Off-the-shelf components: ≥ 80% COTS parts

---

### 7. OPERATIONAL REQUIREMENTS

#### 7.1 Modes of Operation
**Mode 1: Automatic** - Full autonomous operation using sensors

**Mode 2: Energy Saver** - Aggressive energy conservation, lower light levels

**Mode 3: Manual** - User-controlled, overrides automatic functions

**Mode 4: Presentation** - Preset lighting for specific activities

**Mode 5: Maintenance** - Diagnostic mode, all sensors/actuators testable

#### 7.2 Operational Scenarios
**OR-001**: Normal office hours operation (8 AM - 6 PM)

**OR-002**: After-hours security lighting (6 PM - 8 AM)

**OR-003**: Weekend/holiday minimal operation

**OR-004**: Emergency override (fire alarm integration)

**OR-005**: Maintenance mode (system diagnostics)

---

### 8. VERIFICATION & VALIDATION REQUIREMENTS

#### 8.1 Testing Requirements
**VR-001**: Unit testing for all software modules: 100% code coverage

**VR-002**: Integration testing for sensor-controller-actuator chain

**VR-003**: System testing under various lighting conditions

**VR-004**: Performance testing for response times and accuracy

**VR-005**: Reliability testing: 72-hour continuous operation

**VR-006**: User acceptance testing with minimum 5 test subjects

#### 8.2 Acceptance Criteria
**AC-001**: All Level 0 and Level 1 requirements met

**AC-002**: Energy savings demonstrated: ≥ 30%

**AC-003**: User satisfaction score: ≥ 4.0/5.0

**AC-004**: Zero critical safety issues

**AC-005**: Documentation complete: User manual, technical specs, maintenance guide

---

## 🔍 CONCEPT OF OPERATIONS (ConOps)

### Typical Use Case Scenario:

**Morning (8:00 AM)**
1. Employee enters room (previously unoccupied)
2. PIR sensor detects motion within 200ms
3. Light sensor reads ambient light: 150 lux (insufficient)
4. Controller calculates required artificial light: 350 lux
5. LED driver ramps up to 60% intensity over 1.5 seconds
6. Target illumination achieved: 500 lux total

**Mid-Day (12:00 PM)**
1. Sunlight increases ambient light to 400 lux
2. Light sensor detects change
3. Controller reduces artificial light to 20% intensity
4. Target illumination maintained: 500 lux total
5. Energy saved: 80% compared to full brightness

**Evening (6:30 PM)**
1. Employee leaves room
2. No motion detected for 5 minutes
3. Controller initiates fade-out sequence
4. Lights dim to 0% over 2 seconds
5. System enters standby mode (<0.5W consumption)

**Presentation Mode**
1. User presses "Mode" button twice
2. System enters Presentation mode
3. Lights dim to 30% for projector visibility
4. Motion timeout extended to 30 minutes
5. Ambient light sensing disabled temporarily

---

## 📈 TECHNICAL PERFORMANCE MEASURES (TPMs)

### Primary TPMs:
1. **Energy Consumption Reduction**: 30-40% target
2. **Occupancy Detection Accuracy**: ≥95% target
3. **Illumination Level Accuracy**: ±50 lux target
4. **System Response Time**: ≤2 seconds target
5. **System Availability**: ≥99.5% target

### Success Criteria Matrix:

| TPM | Threshold | Objective | Stretch Goal |
|-----|-----------|-----------|--------------|
| Energy Savings | 25% | 30% | 40% |
| Detection Accuracy | 90% | 95% | 98% |
| Response Time | 3 sec | 2 sec | 1 sec |
| False Positives | <5% | <2% | <1% |
| User Satisfaction | 3.5/5 | 4.0/5 | 4.5/5 |

---

## 🎯 REQUIREMENTS TRACEABILITY MATRIX (RTM)

| Req ID | Parent | Verification Method | Priority | Status |
|--------|--------|-------------------|----------|--------|
| MR-001 | - | Test | Critical | Defined |
| MR-002 | - | Analysis | High | Defined |
| MR-003 | - | Test | Critical | Defined |
| FR-001 | MR-001 | Test | Critical | Defined |
| FR-005 | MR-001 | Test | High | Defined |
| FR-009 | MR-003 | Test | High | Defined |
| PR-001 | FR-001 | Test | Medium | Defined |
| PR-009 | MR-002 | Analysis | High | Defined |

---

## 🔄 REQUIREMENTS VALIDATION STATUS

### Phase A Completion Criteria:
- ✅ All stakeholders identified and engaged
- ✅ Mission requirements defined and approved
- ✅ Functional requirements documented (24 requirements)
- ✅ Performance requirements specified (16 requirements)
- ✅ Interface requirements established (12 requirements)
- ✅ ConOps documented with use cases
- ✅ TPMs defined with measurable criteria
- ✅ RTM initiated for traceability

### Phase A Decision Gate:
**Status**: READY FOR PHASE B - PRELIMINARY DESIGN

**Approval**: Requirements baseline established and locked for Phase B entry

**Next Steps**: 
1. Begin architecture trade studies
2. Develop preliminary system design
3. Component selection and preliminary BOM
4. Risk analysis and mitigation planning

---

## 📝 ASSUMPTIONS & CONSTRAINTS

### Assumptions:
1. Standard office environment (no harsh industrial conditions)
2. Existing electrical infrastructure supports dimming
3. WiFi network available for connectivity
4. Users have basic technical literacy
5. Maintenance performed annually

### Constraints:
1. Budget limited to $500 for prototype
2. Must use off-the-shelf components
3. Installation without structural modifications
4. Compliance with local electrical codes
5. 12-week development timeline

---

## 🚀 PHASE A EXIT CRITERIA

- [x] Requirements Review Board approval
- [x] Stakeholder sign-off on requirements
- [x] ConOps validated with end-users
- [x] Technical feasibility confirmed
- [x] Budget and schedule baseline established
- [x] Risk register initiated
- [x] Requirements baseline entered into configuration management



# Intelligent Room Lighting Control System
- Phase B
### Preliminary Design & Technology Completion

---

## 📋 Phase B Overview




**Key Deliverables**:
- System architecture and design
- Component selection with justification
- Preliminary schematics and diagrams
- Risk analysis and mitigation plan
- Cost and schedule baseline

---

## 🏗️ SYSTEM ARCHITECTURE

### 1. HIGH-LEVEL SYSTEM ARCHITECTURE

```
┌─────────────────────────────────────────────────────────────┐
│                    EXTERNAL ENVIRONMENT                      │
│  (Occupants, Natural Light, Room Conditions)                │
└────────────────────┬────────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────────┐
│                   SENSING SUBSYSTEM                          │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────┐       │
│  │ PIR Motion  │  │ Light Sensor │  │  Temperature │       │
│  │   Sensor    │  │  (BH1750)    │  │   Sensor     │       │
│  └──────┬──────┘  └──────┬───────┘  └──────┬───────┘       │
└─────────┼─────────────────┼──────────────────┼──────────────┘
          │                 │                  │
          │                 │                  │
┌─────────▼─────────────────▼──────────────────▼──────────────┐
│              CONTROL & PROCESSING SUBSYSTEM                  │
│  ┌──────────────────────────────────────────────────┐       │
│  │         ESP32 Microcontroller                     │       │
│  │  ┌────────────────┐  ┌─────────────────┐        │       │
│  │  │ Sensor Fusion  │  │  Control Logic  │        │       │
│  │  │    Module      │  │   (PID + FSM)   │        │       │
│  │  └────────┬───────┘  └────────┬────────┘        │       │
│  │           │                    │                  │       │
│  │  ┌────────▼────────────────────▼────────┐        │       │
│  │  │    Decision Engine & Scheduler       │        │       │
│  │  └────────┬─────────────────────────────┘        │       │
│  │           │                                       │       │
│  │  ┌────────▼────────┐  ┌──────────────────┐      │       │
│  │  │ Data Logging    │  │  Web Server      │      │       │
│  │  │ & Analytics     │  │  (HTTP/MQTT)     │      │       │
│  │  └─────────────────┘  └──────────────────┘      │       │
│  └──────────────────────────┬───────────────────────┘       │
└─────────────────────────────┼─────────────────────────────┬─┘
                              │                             │
┌─────────────────────────────▼─────────────────────────────▼─┐
│               ACTUATION SUBSYSTEM                            │
│  ┌────────────────┐  ┌─────────────────┐  ┌──────────────┐ │
│  │ LED Driver     │  │  Relay Module   │  │ Status LEDs  │ │
│  │ (PWM/0-10V)    │  │  (On/Off)       │  │ (Indicators) │ │
│  └────────┬───────┘  └────────┬────────┘  └──────┬───────┘ │
└───────────┼──────────────────┼────────────────────┼─────────┘
            │                  │                    │
┌───────────▼──────────────────▼────────────────────▼─────────┐
│                  USER INTERFACE SUBSYSTEM                    │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────┐       │
│  │  Physical   │  │ Web Dashboard│  │ Mobile App   │       │
│  │  Buttons    │  │  (Browser)   │  │  (Optional)  │       │
│  └─────────────┘  └──────────────┘  └──────────────┘       │
└──────────────────────────────────────────────────────────────┘
```

### 2. FUNCTIONAL DECOMPOSITION

#### 2.1 Sensing Subsystem Functions
- **F1.1**: Detect human occupancy (presence/absence)
- **F1.2**: Measure ambient light levels (0-10,000 lux)
- **F1.3**: Monitor environmental conditions (temperature, humidity)
- **F1.4**: Filter and condition sensor signals
- **F1.5**: Detect sensor faults and anomalies

#### 2.2 Control & Processing Functions
- **F2.1**: Acquire and process sensor data at 10 Hz
- **F2.2**: Execute control algorithms (PID for dimming)
- **F2.3**: Implement finite state machine for mode management
- **F2.4**: Log historical data for analytics
- **F2.5**: Communicate via WiFi (HTTP/MQTT protocols)
- **F2.6**: Implement watchdog and fault recovery

#### 2.3 Actuation Functions
- **F3.1**: Generate PWM signals for dimming (0-100%)
- **F3.2**: Control relay for on/off switching
- **F3.3**: Drive status indicators (RGB LEDs)
- **F3.4**: Implement smooth transitions (fade effects)

#### 2.4 User Interface Functions
- **F4.1**: Accept manual input (buttons/touch)
- **F4.2**: Display system status visually
- **F4.3**: Serve web interface for monitoring
- **F4.4**: Support configuration changes remotely

---

## 🔧 COMPONENT SELECTION & TRADE STUDIES

### Trade Study 1: Microcontroller Selection

| Criterion | Weight | Arduino Uno | ESP32 | Raspberry Pi Zero |
|-----------|--------|-------------|-------|-------------------|
| Processing Power | 20% | 5 | 9 | 10 |
| WiFi Built-in | 25% | 0 | 10 | 10 |
| Cost | 20% | 8 | 9 | 6 |
| Power Consumption | 15% | 7 | 8 | 4 |
| Community Support | 10% | 10 | 9 | 8 |
| GPIO Availability | 10% | 6 | 9 | 7 |
| **Weighted Score** | - | **5.35** | **8.85** | **7.65** |

**Selection: ESP32 DevKit V1**
- **Justification**: Best overall score, built-in WiFi/Bluetooth, dual-core processor, 34 GPIO pins, extensive library support
- **Cost**: $8-12
- **Power**: 80mA active, <10µA deep sleep

### Trade Study 2: Motion Sensor Selection

| Criterion | Weight | PIR (HC-SR501) | Microwave (RCWL-0516) | Ultrasonic | IR Array |
|-----------|--------|----------------|----------------------|------------|----------|
| Detection Range | 20% | 8 | 9 | 7 | 6 |
| False Positive Rate | 25% | 7 | 6 | 8 | 9 |
| Cost | 20% | 9 | 9 | 7 | 4 |
| Power Consumption | 15% | 8 | 7 | 6 | 5 |
| Easy Integration | 20% | 10 | 8 | 7 | 6 |
| **Weighted Score** | - | **8.20** | **7.65** | **7.10** | **6.30** |

**Selection: PIR Motion Sensor (HC-SR501)**
- **Justification**: Best balance of accuracy, cost, and ease of integration
- **Cost**: $2-3
- **Range**: 5-7 meters
- **Detection Angle**: 120°

### Trade Study 3: Light Sensor Selection

| Criterion | Weight | BH1750 | TSL2561 | LDR (Photoresistor) | VEML7700 |
|-----------|--------|--------|---------|---------------------|----------|
| Accuracy | 30% | 9 | 8 | 4 | 10 |
| Range (lux) | 25% | 9 | 8 | 6 | 9 |
| Digital Interface | 20% | 10 | 10 | 0 | 10 |
| Cost | 15% | 8 | 7 | 10 | 6 |
| Calibration Ease | 10% | 9 | 8 | 3 | 9 |
| **Weighted Score** | - | **8.90** | **8.15** | **4.45** | **9.00** |

**Selection: VEML7700 (Primary), BH1750 (Backup)**
- **Justification**: Highest accuracy, wide dynamic range, I2C interface
- **Cost**: $4-6
- **Range**: 0.0036 to 120,796 lux
- **Resolution**: 16-bit

### Trade Study 4: LED Driver Selection

| Option | Type | Cost | Dimming | Complexity | Selected |
|--------|------|------|---------|------------|----------|
| MOSFET PWM | Analog | $3 | 0-100% | Low | ✓ Primary |
| 0-10V Driver | Analog | $15 | 0-100% | Medium | Alternative |
| DALI Driver | Digital | $35 | 0-100% | High | Future |
| Phase Cut Dimmer | AC | $12 | 0-100% | Medium | N/A |

**Selection: N-Channel MOSFET (IRLZ44N) with PWM**
- **Justification**: Cost-effective, simple implementation, adequate performance
- **Cost**: $1-2 per channel
- **Switching Frequency**: 1-5 kHz PWM

---

## 📊 PRELIMINARY BILL OF MATERIALS (BOM)

| Item | Part Number | Quantity | Unit Cost | Total Cost | Supplier |
|------|-------------|----------|-----------|------------|----------|
| **Processing** |
| ESP32 DevKit V1 | ESP32-WROOM-32 | 1 | $10.00 | $10.00 | Amazon/AliExpress |
| **Sensors** |
| Light Sensor | VEML7700 | 1 | $5.00 | $5.00 | Adafruit |
| PIR Motion Sensor | HC-SR501 | 2 | $2.50 | $5.00 | Amazon |
| Temperature Sensor | DHT22 | 1 | $4.00 | $4.00 | Amazon |
| **Actuators** |
| MOSFET Driver | IRLZ44N | 2 | $1.50 | $3.00 | Mouser |
| Relay Module | 5V 2-Channel | 1 | $3.00 | $3.00 | Amazon |
| Status LEDs (RGB) | WS2812B | 3 | $0.50 | $1.50 | AliExpress |
| **Power Supply** |
| AC-DC Converter | HLK-PM01 (5V 3A) | 1 | $8.00 | $8.00 | Amazon |
| Buck Converter | LM2596 (12V) | 1 | $3.00 | $3.00 | Amazon |
| **User Interface** |
| Push Buttons | Tactile 12mm | 4 | $0.25 | $1.00 | Amazon |
| OLED Display | SSD1306 128x64 | 1 | $6.00 | $6.00 | Amazon |
| **Passive Components** |
| Resistors | Various | 20 | $0.05 | $1.00 | Bulk |
| Capacitors | Various | 10 | $0.10 | $1.00 | Bulk |
| Terminal Blocks | Screw Type | 8 | $0.50 | $4.00 | Amazon |
| **Mechanical** |
| Enclosure | ABS Plastic Box | 1 | $8.00 | $8.00 | Amazon |
| PCB Prototype Board | 10x15cm | 1 | $3.00 | $3.00 | Amazon |
| Wire/Cables | 22AWG Stranded | 5m | $0.50/m | $2.50 | Hardware |
| **LED Lighting** |
| LED Strip/Bulb | 12V Dimmable | 2 | $12.00 | $24.00 | Amazon |
| LED Connectors | DC Barrel | 4 | $1.00 | $4.00 | Amazon |
| **Miscellaneous** |
| Solder/Flux | - | 1 | $5.00 | $5.00 | Hardware |
| Heat Shrink Tubing | Assorted | 1 | $3.00 | $3.00 | Hardware |
| Mounting Hardware | Screws/Standoffs | 1 | $4.00 | $4.00 | Hardware |
| **TOTAL** | | | | **$108.00** | |
| **Contingency (20%)** | | | | **$21.60** | |
| **GRAND TOTAL** | | | | **$129.60** | |

**Note**: Well under $500 budget, allowing for additional features, backup components, and testing materials.

---

## 📐 PRELIMINARY SCHEMATIC DESIGN

### System Block Diagram

```
Power Supply (120VAC)
      │
      ├─→ HLK-PM01 (5V 3A) ──→ ESP32, Sensors, Relays
      │
      └─→ LM2596 (12V 2A) ──→ LED Strips, MOSFET Drivers

ESP32 GPIO Allocation:
├─ GPIO34 (ADC): PIR Sensor 1 Input
├─ GPIO35 (ADC): PIR Sensor 2 Input
├─ GPIO21 (I2C SDA): Light Sensor, OLED Display
├─ GPIO22 (I2C SCL): Light Sensor, OLED Display
├─ GPIO25 (DAC/PWM): LED Dimming Channel 1
├─ GPIO26 (DAC/PWM): LED Dimming Channel 2
├─ GPIO27: Relay Control
├─ GPIO32: Status LED (WS2812B) Data
├─ GPIO33: Temperature Sensor (DHT22)
├─ GPIO13: Button 1 (Mode)
├─ GPIO12: Button 2 (Brightness Up)
├─ GPIO14: Button 3 (Brightness Down)
└─ GPIO15: Button 4 (Override)

Control Flow:
1. Sensors → ESP32 (Read at 10 Hz)
2. ESP32 → Sensor Fusion & Processing
3. ESP32 → Control Algorithm (PID + FSM)
4. ESP32 → PWM/Relay Output
5. ESP32 ⟷ Web Server (WiFi)
```

### Control Algorithm Flow

```
┌─────────────────────────────────────────┐
│         MAIN CONTROL LOOP (10 Hz)       │
└──────────────┬──────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│      Read All Sensor Inputs              │
│  - PIR Motion (Digital)                  │
│  - Ambient Light (I2C)                   │
│  - Temperature (1-Wire)                  │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│     Sensor Fusion & Filtering            │
│  - Moving Average Filter (N=5)           │
│  - Occupancy State Machine               │
│  - Anomaly Detection                     │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│      Determine Operating Mode            │
│  - Auto / Manual / Energy-Saver          │
│  - Check Manual Override                 │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│    Calculate Target Illumination        │
│  - Base on occupancy & ambient light     │
│  - Apply mode-specific adjustments       │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│         PID Controller                   │
│  Error = Target - Current                │
│  Output = Kp*E + Ki*∫E + Kd*dE/dt       │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│      Actuator Command Generation         │
│  - PWM Duty Cycle (0-255)                │
│  - Relay On/Off Command                  │
│  - Smooth Transition Logic               │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│      Output to Actuators                 │
│  - LED Driver (PWM)                      │
│  - Relay Module                          │
│  - Status Indicators                     │
└──────────────┬───────────────────────────┘
               │
               ▼
┌──────────────────────────────────────────┐
│      Data Logging & Communication        │
│  - Log to SPIFFS/SD Card                 │
│  - Send to Web Dashboard                 │
│  - Update MQTT Broker (optional)         │
└──────────────────────────────────────────┘
```

---

## 🎛️ CONTROL SYSTEM DESIGN

### PID Controller Parameters

**Tuning Method**: Ziegler-Nichols with empirical adjustment

**Initial Parameters**:
- **Kp (Proportional)**: 2.5
- **Ki (Integral)**: 0.5
- **Kd (Derivative)**: 0.8

**Control Equation**:
```
u(t) = Kp·e(t) + Ki·∫e(t)dt + Kd·de(t)/dt

Where:
- e(t) = Target_Lux - Measured_Lux
- u(t) = PWM duty cycle (0-255)
```

**Anti-Windup**:
- Integral term limited to ±50
- Reset integral when error changes sign

**Output Saturation**:
- Minimum: 0 (lights off)
- Maximum: 255 (100% brightness)

### Finite State Machine (FSM)

```
States:
┌─────────────┐
│   STANDBY   │ ← System powered, no occupancy
└──────┬──────┘
       │ Motion Detected
       ▼
┌─────────────┐
│   ACTIVE    │ ← Normal operation, lights controlled
└──────┬──────┘
       │ No motion for timeout
       ▼
┌─────────────┐
│   GRACE     │ ← Grace period (5 min), ready to reactivate
└──────┬──────┘
       │ Timeout expires
       ▼
┌─────────────┐
│   FADEOUT   │ ← Dimming lights to off (2 sec)
└──────┬──────┘
       │ Fade complete
       ▼
    STANDBY

Special States:
┌─────────────┐
│   OVERRIDE  │ ← Manual control active
└─────────────┘
┌─────────────┐
│  EMERGENCY  │ ← Fire alarm or fault condition
└─────────────┘
```

---

## ⚠️ RISK ANALYSIS & MITIGATION

### Risk Register

| ID | Risk | Probability | Impact | Score | Mitigation Strategy |
|----|------|-------------|--------|-------|---------------------|
| R1 | False positive occupancy detection | Medium | Medium | 6 | Dual PIR sensors, majority voting |
| R2 | WiFi connectivity loss | High | Low | 6 | Local autonomous operation, log buffering |
| R3 | Sensor drift over time | Low | Medium | 4 | Periodic auto-calibration routine |
| R4 | Power supply failure | Low | High | 8 | Graceful degradation, watchdog reset |
| R5 | PWM flicker visible to users | Medium | Low | 4 | High frequency PWM (5 kHz), filter |
| R6 | Integration complexity | Medium | Medium | 6 | Modular design, unit testing |
| R7 | Ambient light sensor saturation | Low | Medium | 4 | Auto-ranging algorithm |
| R8 | User dissatisfaction with automation | Medium | High | 9 | Manual override always available |
| R9 | Component availability delays | Low | Medium | 4 | Multiple supplier sources identified |
| R10 | Budget overrun | Low | High | 8 | 20% contingency, prioritized features |

### Risk Mitigation Details

**R1: False Positive Detection**
- **Mitigation**: Implement two PIR sensors at different angles, require both to trigger
- **Backup**: Adjustable sensitivity and timeout parameters
- **Verification**: 72-hour continuous testing in real environment

**R4: Power Supply Failure**
- **Mitigation**: Brownout detection, safe shutdown sequence, LED fault indicator
- **Backup**: Battery backup for controller (optional, Phase C consideration)
- **Verification**: Power interruption testing

**R8: User Dissatisfaction**
- **Mitigation**: Physical override button always accessible, multiple operating modes
- **Backup**: Web interface for per-user customization
- **Verification**: User acceptance testing with ≥5 subjects

---

## 📅 PRELIMINARY SCHEDULE

### Phase B Activities :

| Week | Activities | Deliverables | Dependencies |
|------|------------|--------------|--------------|
| **Week 2** | System architecture design<br>Trade studies<br>Component selection | Architecture document<br>Trade study reports<br>Preliminary BOM | Phase A requirements |
| **Week 3** | Schematic design<br>Control algorithm development<br>Risk analysis | Preliminary schematics<br>Algorithm pseudocode<br>Risk register | Component selection |
| **Week 4** | Design review preparation<br>Prototype planning<br>PDR presentation | PDR package<br>Detailed work plan<br>Updated schedule | All Phase B activities |

### Overall Project Timeline:

```
Phase A: Requirements     [Weeks 1]     ✓ Complete
Phase B: Prelim Design    [Weeks 2-4]   ← Current Phase
Phase C: Detailed Design  [Weeks 5-6]   
Phase D: Fabrication      [Weeks 7-8]   
Phase E: Integration      [Weeks 9-10]  
Phase F: Testing & Close  [Weeks 11-12] 
```

---

## 💰 COST ANALYSIS

### Cost Breakdown by Subsystem:

| Subsystem | Components Cost | Labor (hrs) | Total |
|-----------|----------------|-------------|-------|
| Processing | $10 | 8 | $10 |
| Sensing | $14 | 6 | $14 |
| Actuation | $7.50 | 10 | $7.50 |
| Power | $11 | 6 | $11 |
| User Interface | $7 | 8 | $7 |
| Mechanical | $15.50 | 12 | $15.50 |
| LED Load | $28 | 4 | $28 |
| Miscellaneous | $15 | 6 | $15 |
| **Subtotal** | **$108** | **60 hrs** | **$108** |
| **Contingency (20%)** | **$21.60** | - | **$21.60** |
| **TOTAL** | **$129.60** | **60 hrs** | **$129.60** |

**Budget Status**: $370.40 under budget (74% under)

**Labor Estimate**: 60 hours @ educational project (not costed)

---

## 🔍 VERIFICATION & VALIDATION PLAN

### Verification Activities (Phase E):

1. **Unit Testing**
   - Each sensor module independently
   - Control algorithm with simulated inputs
   - Actuator response verification
   - Communication protocols

2. **Integration Testing**
   - Sensor-to-controller data flow
   - Controller-to-actuator commands
   - End-to-end system response
   - Error handling and recovery

3. **System Testing**
   - Functional requirements verification
   - Performance requirements validation
   - Environmental condition testing
   - Long-duration reliability test (72 hrs)

### Validation Activities (Phase F):

1. **User Acceptance Testing**
   - Real-world deployment (test room)
   - User satisfaction surveys
   - Energy consumption measurement
   - Usability evaluation

2. **Requirements Traceability**
   - Each requirement mapped to test case
   - Test results documented
   - Non-compliance items identified
   - Waivers/deviations processed

---

## 📋 PHASE B EXIT CRITERIA

### Preliminary Design Review (PDR) Checklist:

- [x] System architecture defined and documented
- [x] All major components selected with trade study justification
- [x] Preliminary BOM complete with costs
- [x] Control algorithms defined with flowcharts
- [x] Risk analysis completed with mitigation plans
- [x] Preliminary schedule established
- [x] Cost estimate within budget
- [x] Interface definitions documented
- [x] Design margins identified
- [x] Verification approach defined
- [x] PDR presentation prepared

### PDR Decision Gate:

**Readiness Assessment**: ✅ **READY FOR PDR**

**Technical Maturity**: System architecture baselined, design approach validated

**Risk Posture**: 10 risks identified, mitigation strategies defined, no show-stoppers

**Cost/Schedule**: On budget ($129.60 of $500), on schedule (Week 4 of 12)

**Recommendation**: **PROCEED TO PHASE C - DETAILED DESIGN**

---

## 🚀 NEXT STEPS 

### Phase C Activities:

1. **Detailed Electrical Design**
   - Complete circuit schematics
   - PCB layout design
   - Power distribution analysis
   - EMI/EMC considerations

2. **Software Architecture**
   - Detailed firmware design
   - State machine implementation
   - Communication protocols
   - Web interface mockups

3. **Mechanical Design**
   - Enclosure CAD modeling
   - Thermal analysis
   - Mounting solutions
   - Cable management

4. **Test Planning**
   - Detailed test procedures
   - Test equipment identification
   - Acceptance criteria refinement
   - Test data collection forms

5. **Critical Design Review (CDR)**
   - Final design package
   - Updated risk assessment
   - Procurement planning
   - Manufacturing readiness

---

## 📊 TECHNICAL PERFORMANCE MEASURES - PHASE B

| TPM | Target | Preliminary Design Prediction | Margin | Status |
|-----|--------|------------------------------|--------|--------|
| Energy Savings | 30% | 35% | +5% | Green |
| Detection Accuracy | 95% | 96% (dual sensor) | +1% | Green |
| Response Time | 2.0 sec | 1.5 sec | +0.5 sec | Green |
| System Cost | $500 | $130 | +$370 | Green |
| False Positive Rate | <2% | 1.5% | +0.5% | Green |

**All TPMs tracking positively - Low risk to meeting requirements**

---

## 📝 DESIGN DECISIONS LOG

| Decision # | Topic | Options Considered | Selected | Rationale | Date |
|------------|-------|-------------------|----------|-----------|------|
| DD-01 | Controller | Arduino, ESP32, RPi | ESP32 | WiFi, processing power, cost | Week 2 |
| DD-02 | Motion Sensor | PIR, Microwave, US | PIR (dual) | Accuracy, cost, false pos. | Week 2 |
| DD-03 | Light Sensor | BH1750, VEML7700 | VEML7700 | Accuracy, range, resolution | Week 3 |
| DD-04 | LED Driver | PWM, 0-10V, DALI | PWM MOSFET | Cost, simplicity, adequate | Week 3 |
| DD-05 | Power Supply | Linear, Switching | Switching | Efficiency, heat, size | Week 3 |
| DD-06 | Communication | WiFi, Zigbee, BLE | WiFi | Infrastructure exists, range | Week 2 |

---

