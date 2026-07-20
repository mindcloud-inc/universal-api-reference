# Get Ticket Types for Event with Products with Eventix

Retrieves ticket types with products for an Eventix event.

## Endpoint

- **Method:** `GET`
- **Path:** `/3.0.0/event/:guid/ticket/products`
- **Base URL:** `https://api.weeztix.com`
- **Official documentation:** [Get Ticket Types for Event with Products](https://docs.weeztix.com/api/dashboard/get-event-tickets-with-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | path | `string` | yes | The guid of the Event. |
