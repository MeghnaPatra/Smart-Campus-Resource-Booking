# Smart-Campus-Resource-Booking
# Smart Campus Resource Booking System 🏫

A full-stack smart campus resource management and booking system designed to simplify the process of discovering, reserving, and managing campus resources.

The system provides a centralized platform for managing resources, handling bookings, validating availability, and supporting notifications and analytics.

## Overview

Managing classrooms, laboratories, meeting rooms, and other campus resources can become difficult when availability and bookings are handled manually.

The Smart Campus Resource Booking System provides a centralized digital platform where users can view available resources, make bookings, and manage their reservations while administrators can manage resources and monitor booking activity.

## Key Features

- 🔐 User authentication and authorization
- 👤 JWT-based authentication
- 🏫 Campus resource management
- 📅 Resource booking and reservation management
- ⏰ Start and end time validation
- 🚫 Prevention of overlapping bookings
- 👥 Resource capacity validation
- 🔔 Notification service
- 📊 Booking and resource analytics
- 🗄️ MongoDB-based data storage
- ⚡ Redis integration
- 📨 Event-driven communication using Kafka
- 🐳 Docker-based deployment and service management

## System Architecture

```text
                    ┌─────────────────────┐
                    │      Frontend       │
                    │   User Interface    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Authentication   │
                    │    & Authorization  │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
       ┌────────────┐   ┌────────────┐   ┌────────────┐
       │  Resource  │   │  Booking   │   │Notification│
       │  Service   │   │  Service   │   │  Service   │
       └──────┬─────┘   └──────┬─────┘   └──────┬─────┘
              │                │                │
              └────────────────┼────────────────┘
                               │
                ┌──────────────┴──────────────┐
                │                             │
                ▼                             ▼
         ┌────────────┐                 ┌────────────┐
         │  MongoDB   │                 │   Redis    │
         └────────────┘                 └────────────┘
                              
                       ┌────────────┐
                       │   Kafka    │
                       │  / Events  │
                       └────────────┘
