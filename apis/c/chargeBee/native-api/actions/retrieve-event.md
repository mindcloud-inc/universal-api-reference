# Retrieve Event with ChargeBee

Retrieves an event from ChargeBee.

## Endpoint

- **Method:** `GET`
- **Path:** `events/:event_id`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Retrieve Event](https://apidocs.chargebee.com/docs/api/events/retrieve-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Chargebee event identifier. |
