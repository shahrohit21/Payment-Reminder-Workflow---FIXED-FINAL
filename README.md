# AI-Powered Payment Reminder Workflow

## Overview

This project automates overdue payment follow-ups using n8n, WhatsApp, Google Sheets, AI voice calls, and OpenAI.

The workflow identifies customers with outstanding balances, sends automated reminder messages at different stages, triggers AI-powered voice calls for severely overdue payments, and records all interactions in Google Sheets.

## Features

* Automated daily payment monitoring
* Google Sheets integration for invoice and payment tracking
* WhatsApp reminder automation
* Multi-stage reminder system

  * First Reminder
  * Second Reminder
  * Final Reminder
* AI Voice Call escalation for highly overdue payments
* Customer response classification using OpenAI
* Automatic follow-up scheduling
* Reminder history tracking

## Workflow Logic

### Stage 1: Data Collection

* Runs daily at scheduled time
* Reads customer payment data from Google Sheets
* Filters records with pending balances

### Stage 2: Reminder Decision Engine

* Checks overdue days
* Determines appropriate action:

  * WhatsApp Reminder 1
  * WhatsApp Reminder 2
  * WhatsApp Reminder 3
  * AI Voice Call
  * Skip if payment is completed

### Stage 3: Automated Communication

* Sends personalized WhatsApp reminders
* Includes:

  * Customer name
  * Bill number
  * Invoice amount
  * Outstanding balance
  * Overdue days

### Stage 4: AI Voice Call Escalation

For invoices overdue beyond the defined threshold:

* Initiates AI-powered phone call
* Collects customer response
* Records conversation outcome

### Stage 5: AI Response Analysis

OpenAI classifies customer responses into categories:

* PAYMENT_DONE
* PROMISE_TO_PAY
* NEED_TIME
* DISPUTE
* CALLBACK_REQUESTED
* NOT_AVAILABLE
* NO_ANSWER
* NO_RESPONSE
* OTHER

### Stage 6: Follow-Up Management

* Updates reminder history
* Stores customer responses
* Schedules future follow-ups automatically

## Tech Stack

* n8n
* Google Sheets
* WhatsApp Business API
* OpenAI GPT
* Retell AI
* JavaScript

## Business Benefits

* Reduces manual collection efforts
* Improves payment recovery process
* Ensures timely customer follow-ups
* Maintains complete communication history
* Scales collection operations efficiently

## Future Improvements

* Email reminders
* Dashboard reporting
* Payment gateway integration
* CRM integration
* Advanced analytics

## Author

Rohit Shah

AI Automation | n8n | OpenAI | Workflow Automation
