# Tui Tracker

# Using Photo Analytics to help bring the Tui Back to Christchurch

# Project Goals
TBD

# Architecture
![Markdown Logo](https://github.com/Kwesi-Peterson/Tui-Tracker/blob/main/images/TuiTrackerArchitecture.jpg)

[Inspired by the Project 15 IOT Sustainability Architecture](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/project-15-iot-sustainability)

1) The Azure IoT Hub device provisioning service provisions IoT devices and connects them to IoT Hub. The main IoT device that will be used is a Raspberry Pi to capture images.
2) Streaming platforms and services build the data pipeline that's necessary for basic telemetry and event processing:
- Azure Event Hubs ingests telemetry and events from IoT devices.
3) Azure Functions will use Cognitive Service - Vision to filter all the images containing Tui.
4) The solution will batch process the images and store them in Azure Data Lake
5) Power BI will be used to visualise the data
6) Finally, data captured here will be added to Azure ML to improve the AI model used to identify TUI
