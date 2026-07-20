# Show Email Activity Logs with Cakemail

Retrieves email activity logs from Cakemail.

## Endpoint

- **Method:** `GET`
- **Path:** `/logs/emails`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Show Email Activity Logs](https://cakemail.dev/en/api/log#show-email-activity-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `log_type` | query | `string` | yes | Email log type to retrieve. Use sent, bounce, clickthru, open, unsubscribe, resubscribe, spam, global_unsubscribe, or all. Cakemail currently returns an upstream 500 for all on this tenant; sent is the safe default. |
