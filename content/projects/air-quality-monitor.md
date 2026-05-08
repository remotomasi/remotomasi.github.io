---
title: "ESP32 Air Quality Monitor"
date: 2026-05-01
tags: ["ESP32", "KiCad", "C", "FreeRTOS", "sensori"]
draft: false
cover:
  image: /images/projects/air-quality-monitoring/preview.jpeg
  alt: "Air Quality Monitor"
summary: "Dispositivo indoor per il monitoraggio della qualità dell'aria basato su ESP32."
---

## Obiettivo

Monitoraggio in tempo reale di CO, CO₂, VOC e particolato fine in ambienti indoor.

## Hardware

- **MCU**: ESP32-WROOM-32
- **Sensori gas**: MQ-2, MQ-4, MQ-7, ENS160 + AHT21
- **Sensore ambientale**: AHT21
- **Particolato**: PMS5003
- **Design PCB**: KiCad 9

![Schema elettrico](/images/projects/air-quality-monitoring/aqm.png)

## Firmware

- ESP-IDF + FreeRTOS
- MQ-7: ciclo PWM di riscaldamento
- ENS160: lettura event-driven via semaforo
- PMS5003: UART parsing

## Stato

🟡 In sviluppo — schematica completata, firmware in fase di test