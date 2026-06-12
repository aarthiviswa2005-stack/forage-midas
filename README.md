# Midas Core — Banking Transaction System

A real-time banking transaction processing system built with Java Spring Boot and Apache Kafka.

## Tech Stack
- Java 17
- Spring Boot 3.2.5
- Apache Kafka
- H2 Database
- Spring Data JPA
- REST API

## Features
- Real-time transaction processing via Kafka messaging
- Transaction validation (balance check, valid sender/recipient)
- External Incentive API integration using RestTemplate
- REST endpoint `/balance` to query user balances
- Automated test suite with Testcontainers

## How It Works
1. Transactions are sent to a Kafka topic `trader-updates`
2. The Kafka listener validates each transaction
3. Valid transactions update sender and recipient balances in H2 database
4. An incentive bonus is fetched from external API and added to recipient balance
5. All transactions are recorded in the database

## Built As Part Of
JP Morgan Chase & Co. Software Engineering Virtual Experience — Forage (June 2026)
