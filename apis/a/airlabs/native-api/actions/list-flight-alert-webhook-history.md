# List Flight Alert Webhook History with Airlabs

Retrieves flight alert webhook history from Airlabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [List Flight Alert Webhook History](https://airlabs.co/docs/alert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `days` | query | `number` | no | Number of days of webhook history to return. |
| `listener_id` | query | `number` | no | Filter webhook history by listener ID when needed. |
