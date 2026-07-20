# Get API Usage Stats with ContactOut

Retrieves API usage stats for a month in ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/stats`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Get API Usage Stats](https://api.contactout.com/#api-usage-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `period` | query | `string` | no | Month to inspect in YYYY-MM format. If omitted, ContactOut uses the current month. |
