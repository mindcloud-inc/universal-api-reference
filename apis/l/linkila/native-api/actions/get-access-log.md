# Get Access Log with Linkila

Retrieves access log entries from Linkila.

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/accessLog`
- **Base URL:** `https://app.linkila.com/integrations/api/v1`
- **Official documentation:** [Get Access Log](https://app.linkila.com/integrations/api/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | body | `date` | no | Optional ISO date-time cursor; return access-log entries before this timestamp. |
| `limit` | body | `number` | no | Maximum number of access-log entries to return. Official maximum: 500. |
| `filter` | body | `object` | no | Optional Linkila analytics filter object. |
