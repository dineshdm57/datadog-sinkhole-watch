# Datadog Sinkhole Watch

Find and flag silent Datadog monitors that receive data but never trigger alerts.

## Overview

Some monitors quietly consume data without ever alerting. This workflow detects those “sinkholes” so you can disable or fix them.

Built using OpenOps — no coding required.

## What It Does

- Fetches all Datadog monitors
- Checks the last triggered time
- Flags monitors inactive for over 30 days
- Sends alerts to Slack

## Why Use It?

- Cuts down on wasted observability spend
- Improves alert reliability
- Easy to deploy, no code required

## Setup Instructions

1. **Exported Workflow File**: Use the included `.json` file to import into OpenOps.
2. **Connections Required**:
   - Datadog API key (via Send HTTP block)
   - Slack connection (to send results)

3. **Modify if Needed**:
   - Adjust the `30 days` threshold in the loop code block.
   - Customize Slack message formatting if needed.

## Extend It

This template is editable. You can adapt it to:
- Look at dashboards instead of monitors
- Combine with spend data from Datadog billing APIs
- Alert to email or ticketing systems

## Requirements

- Datadog account
- Slack workspace
- OpenOps account

---

Built for ops teams to cut waste, stay alert-ready, and automate cleanup tasks.
