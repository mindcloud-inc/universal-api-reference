# List Events with Morgen

Retrieves events from Morgen.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/events/list`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [List Events](https://docs.morgen.so/events#list-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | Calendar account ID. Defaults to the connection accountId. |
| `calendarIds` | query | `string` | no | Comma-separated calendar IDs. Defaults to the connection calendarId. |
| `start` | query | `string` | yes | Inclusive window start in ISO 8601 UTC format. |
| `end` | query | `string` | yes | Exclusive window end in ISO 8601 UTC format. |
