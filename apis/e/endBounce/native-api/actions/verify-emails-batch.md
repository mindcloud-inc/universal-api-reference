# Verify Emails Batch with EndBounce

Creates a verification job in EndBounce for multiple emails.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verify`
- **Base URL:** `https://api.endbounce.com/api/integrations`
- **Official documentation:** [Verify Emails Batch](https://app.endbounce.com/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Email addresses to verify in one batch request. |
