## Phase 1: Recording a Rap Demo

This plan details the process of recording a rap vocal demo in a forest environment. The artist will perform multiple takes of a 29-second section of a song. The recording will be done directly to the laptop's internal storage, and then backed up to a USB flash drive. The backing track will be played through headphones, without the singer monitoring their own voice.

### 1. Recording Setup

| Device                     | OS | Software                               |
|-----------------------------|--------------------|----------------------------------------|
| Lenovo IdeaPad S120+       | Debian GNU/Linux 12 (Bookworm) | Ardour 7.2, ReaFIR 2.0, qjackctl      |
| Samsung Galaxy S10+        | Android 10         | DecibelX, VLC                           |

#### Microphone: HM-66

Professional dynamic microphone with a cardioid capsule with a pop filter and a 5 meters long XLR-PL microphone cable.

|-----------------|--------------------------------------------------|
| Model            | HM-66                                           |
| Type             | Dynamic Cardioid Microphone                     |
| Connection       | XLR (5m XLR-PL cable)                       |
| Power            | Battery-free                                     |
| Resistance       | 600 ohms                                         |
| Sensitivity      | -63dB                                           |
| Frequency Response| 100Hz-13kHz                                      |
| Features         | Pop filter |

#### Headphones: Jabra Elite 85t

(for backing track playback only)

- **Driver Size**: 12 mm
- **Bluetooth Version**: 5.1
- **Battery Life**: 5.5 to 6.5 hours
- **Water Resistance**: IPX4
- **Frequency Response**: 20 Hz to 20 kHz
- **Impedance**: 16 ohms
- **Sensitivity**: 103 dB SPL/mW


#### Audio Interface: Focusrite Scarlett Solo

(with up-to-date drivers)


## 2. Pre-Production

### 2.1 Software and System Setup

1.  **System Update:** `sudo apt update && sudo apt upgrade`. Ensure sufficient hard drive space.
2.  **JACK Installation:** `sudo apt install jackd2 qjackctl`.
3.  **ReaFIR Installation:** Attempt installation via `sudo apt search reafir` followed by `sudo apt install reafir`. If unsuccessful, use your preferred package manager or download from [Official ReaFIR Download Link] and follow the instructions. Consider `flatpak` or source installation if `apt` fails.
4.  **Ardour Configuration:** Configure Ardour 7.2 for 48kHz, 16-bit stereo. Set an initial buffer size of 256 samples; adjust as needed during latency testing.


### 2.2 Equipment Checks and Connections

1.  **Microphone Inspection:** Visually inspect the HM-66 microphone for damage.
2.  **Cable Inspection:** Visually inspect XLR cables for damage and ensure proper connections.
3.  **Headphone Setup:** Connect the Jabra Elite 85t headphones directly to the Focusrite Scarlett Solo's headphone output. Test headphone volume.
4.  **Interface Connection:** Connect the HM-66 microphone to the Focusrite Scarlett Solo interface.
5.  **Backing Track Transfer:** Transfer the backing track to the laptop.


### 2.3 Testing and Measurement

#### 2.3.1 Latency Assessment

1.  **Click Track Creation:** Create a simple click track in Ardour.
2.  **JACK Configuration:** Start `qjackctl` and configure JACK for your audio interface. Adjust the buffer size as needed.
3.  **Latency Measurement:** Record the click track. Use `qjackctl`'s latency monitoring or Ardour's tools to measure latency.


#### 2.3.2 Gain Staging and Level Calibration

1.  **Test Tone Generation:** Create a -18dBFS test tone in Ardour.
2.  **Gain Adjustment:** Record the test tone. Adjust the Focusrite's gain until peak levels consistently reach approximately -18dBFS. Use a VU meter plugin in Ardour for visual feedback.
3.  **Vocal Test Recording:** Record a short section (16 bars) of the song. Monitor peak levels in Ardour.
4.  **Iterative Refinement:** Repeat step 3, focusing on consistent vocal effort and peak levels.
5.  **Comprehensive Test Recording:** Record a longer section (32 bars or a verse).


### 2.4 Location Scouting and Microphone Placement

1.  **Location Identification:** Explore potential forest locations, considering shelter, accessibility, visual appeal, potential noise sources, and wind protection.
2.  **Ambient Noise Measurement:** Use DecibelX to measure ambient noise levels.
3.  **Acoustic Environment Assessment:** Assess reverberation and interfering sounds.
4.  **Location Selection:** Choose the most suitable location.
5.  **Microphone Placement:** Experiment with microphone heights and angles. Use a windscreen (deadcat) to minimize wind noise. Consider a pop filter.


## 3. Recording: A Detailed Approach

### 3.1 Pre-Recording Checks

1.  **Power Verification:** Check laptop battery level; ensure sufficient charge for the estimated recording time.
2.  **Headphone Check:** Verify comfortable headphone volume and absence of feedback.
3.  **Signal Path Verification:** Double-check all connections. Listen to the test tone.
4.  **Software Setup:** Verify Ardour configuration (48kHz, 16-bit, buffer size), and input/output channel selection.
5.  **Ambient Noise Check:** Perform a final check of ambient noise levels.
6.  **Backing Track Playback Test:** Ensure the backing track plays correctly.


### 3.2 Recording Process

1.  **Level Monitoring:** Maintain consistent levels around -18dBFS in Ardour.
2.  **Routing and Monitoring:** Ensure correct routing in Ardour: microphone input to the recording track, and playback routed to the headphones.
3.  **Cue Mix Setup (Ardour):** Create a separate output bus for the cue mix. Route backing tracks to this bus, then to the headphone output. Adjust levels.
4.  **Take Management:** Record multiple takes using the file naming convention: `ProjectNameXX.wav`. Label takes in Ardour; use markers.
5.  **Performance Guidance:** Self-assessment and self-correction. Provide breaks as needed.
6.  **Weather Monitoring:** Monitor weather conditions.


### 3.3 Troubleshooting Common Issues

*   **Clipping:** Reduce the gain on the Focusrite.
*   **Noise Issues:** Identify the source. Adjust microphone placement or use noise reduction techniques.
*   **Latency Problems:** Adjust the Ardour buffer size.
*   **Technical Malfunctions:** Have backup equipment available (if possible).
*   **Headphone Volume Issues:** Adjust the Focusrite's volume control.
*   **Audio Dropouts:** Check JACK settings and buffer size.
*   **Wind Noise:** Use a windscreen.


### 3.4 Recording Wrap-Up

1.  **Final Level Check:** Review all recorded takes.
2.  **Data Backup:** Immediately back up all recorded audio files to the external SSD.


## 4. Post-Production

(This section would detail the editing, mixing, and mastering process, but is omitted for brevity as it's not directly impacted by the power source change.)
