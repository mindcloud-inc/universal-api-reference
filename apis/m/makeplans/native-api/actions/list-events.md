# List Events with Makeplans

Retrieves events from Makeplans.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [List Events](https://developer.makeplans.com/endpoints/events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | Return events with ends_at before this datetime. |
| `start` | query | `string` | no | Return events with starts_at after this datetime. |
