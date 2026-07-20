# Get Sender Health Summary with SuperSend

Retrieves the sender health summary from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/intelligence/sender-health-summary`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Get Sender Health Summary](https://api.supersend.io/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `string` | yes | Team UUID (from list teams) |
| `windowDays` | query | `number` | no | Days to look back (1-90, default 30) Range: 1 to 90. |
