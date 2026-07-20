# List Zapier Trigger Examples with EventSquare

Retrieves Zapier trigger examples from EventSquare.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/integrations/zapier/triggers`
- **Base URL:** `https://api.eventsquare.io`
- **Official documentation:** [List Zapier Trigger Examples](https://api.eventsquare.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | The EventSquare trigger type to retrieve example webhook payloads for. Accepted values: `0`. |
