# AI Virtual Administrator for Beauty Salon

An n8n-based Telegram assistant I built to automate repetitive communication between a beauty salon and its customers.

The workflow accepts both text and voice messages, uses an LLM to generate responses according to predefined salon rules, collects appointment-related information and can escalate a conversation to a human manager when needed.

## Workflow

![n8n workflow](workflow.png)

The main flow is:

Telegram message  
→ n8n processing  
→ AI response logic  
→ customer reply

If the request requires human involvement, the workflow forwards it to a manager and returns the manager's answer back to the customer.

## Demo

[Watch the demo](demo.mp4)

## What it can do

- process text and voice messages;
- answer common customer questions;
- work in multiple languages;
- follow predefined business instructions;
- collect information needed for an appointment;
- escalate selected requests to a manager;
- return the manager's response to the customer.

## Why I built it

A large part of salon communication consists of repetitive questions about services, prices, availability and appointments.

I wanted to test whether this part of customer communication could be automated without removing the possibility of human intervention when it is actually needed.

## Implementation

The workflow was built in n8n and integrates:

- Telegram Bot API
- OpenAI API
- message routing and branching logic
- prompt-based response rules
- human handoff logic

The exported n8n workflow is available here:

[`telegram_virtual_admin_workflow.json`](telegram_virtual_admin_workflow.json)

## My role

I designed and built the workflow independently, including its structure, prompts, Telegram integration, routing logic and testing.

## Technologies

- n8n
- OpenAI API
- Telegram Bot API
- Prompt Engineering
- Workflow Automation

## Status

This is an independent prototype.

The current version demonstrates the complete communication flow. Possible next steps include appointment-calendar integration and persistent customer data storage.
