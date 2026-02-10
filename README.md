# Call-Logs-Tool
Call Logs Tool
📞 Call Logs Tool

A lightweight, web-based call logging and analytics tool built for support teams.
This application allows agents to log customer calls, track resolutions, and enables admins to analyze activity across agents, companies, and tools — all powered by Firebase (Spark / Free Plan).

🚀 Live Overview

Web-based (no backend server required)

Role-based access (Agent & Admin)

Real-time logging and analytics

CSV export for reporting

Runs entirely on Firebase Free (Spark) plan

🧩 Tech Stack

Frontend

HTML5

CSS3

Vanilla JavaScript

Backend / Services

Firebase Authentication (Email & Password)

Firebase Firestore (NoSQL Database)

Hosting

Static hosting (Firebase Hosting or any static host)

🔐 Authentication & Roles
Authentication

Email & password login via Firebase Authentication

Domain-restricted login (configurable)

Roles

Agent

Create and manage call logs

View personal call history

Track daily performance stats

Admin

View all call logs

Run analytics & leaderboards

Export data as CSV

Delete call logs

Admin access is automatically assigned based on email prefix (configurable).

✨ Features
Call Logging

Customer name & phone number

Reference ID (Order # / User ID / Invoice #)

Tool selection (e.g., Shopify, Marcom, Marketing Bench)

Dynamic company lists per tool

Call disposition & status tracking

Structured notes (Concern / Action Taken)

Search & Filters

Search by customer name

Filter by company

Filter by date range

Sort by most recent activity

Agent Stats

Daily call count

Daily resolved calls

Simple performance snapshot per agent

Admin Analytics

Agent activity leaderboard

Resolution rate per agent

Most-used dispositions

Most-used companies

Date and company-based filtering

Export & Management

One-click CSV export

Admin-only call log deletion

Modal-based note viewer

Toast notifications for user feedback
🗄️ Data Storage (Firestore)
Collection: logs

Each call log document contains:

customer — Customer name

phone — Phone number

ref — Reference ID

tool — Selected tool

company — Company name

disposition — Call disposition

status — Open / Follow-up / Resolved

notes — Call notes

agent — Agent email

created — Firestore server timestamp

createdDay — YYYY-MM-DD

createdMonth — YYYY-MM
Firestore Limits (Spark Plan)

Firebase Spark does not impose a hard limit on the number of documents you can create. Instead, usage is constrained by daily operation quotas and total storage.

Practical Breakdown

Each call log = 1 Firestore document

You can store thousands of call logs

Limits are reached based on:

Daily reads

Daily writes

Total stored data size

Typical Usage Estimate

For a small to medium support team:

~1 log write per call

~10–50 logs per agent per day

Read operations triggered by history views, filters, and analytics

👉 Under normal internal usage, hundreds to thousands of logs per month can be stored comfortably on Spark without issues.

Important Notes

There is no automatic deletion of logs

Logs persist indefinitely until manually deleted

The app is optimized using:

Indexed date fields (createdDay, createdMonth)

Filtered queries to reduce unnecessary reads
📌 README-Ready Summary

On Firebase Spark (Free), this application comfortably supports 10–20 active agents per month under normal usage (10–20 logs per agent per day).
Higher usage may require monitoring Firestore quotas or upgrading to Blaze.
