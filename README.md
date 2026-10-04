# electricity-theft-detection-8051
8051-based current mismatch detection system using ADC0808 and LCD display. MIT Manipal Microcontroller Lab, 2025.

# Electricity Theft Detection System

8051-based system that detects unauthorised current tapping 
between an energy meter and the consumer.

## How it works
Two current sensors feed into an ADC0808 (channels 0 and 1). 
The 8051 reads both channels, computes the absolute difference, 
and triggers a buzzer and LCD alert if the mismatch exceeds 
a set threshold (default: 5 ADC counts).

## Hardware
- AT89C51 (8051 microcontroller)
- ADC0808 (8-channel ADC)
- 16x2 LCD display (P2 data bus, P3 control)
- Piezo buzzer on P3.4
- Two current transformer sensors

## Pin Map
- P1: ADC data output (OUT1–OUT8)
- P2: LCD data
- P3.7 / P3.6 / P3.5: LCD RS / RW / EN
- P0.1–P0.3: ADC address lines A/B/C
- P0.4: ADC Output Enable
- P0.5: ADC Address Latch Enable
- P0.6: ADC Start
- P0.7: ADC End of Conversion
- P3.4: Buzzer

## Status
Completed — September 2025
Built and tested using Keil µVision.

## Files
- main.c — full 8051 C source code
- MICROCONTROLLER_MINI_PROJECT.docx — project report
