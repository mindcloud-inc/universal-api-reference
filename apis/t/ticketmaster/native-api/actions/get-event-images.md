# Get Event Images with Ticketmaster

Retrieves images for a specific event from Ticketmaster.

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery/v2/events/:id/images`
- **Base URL:** `https://app.ticketmaster.com`
- **Official documentation:** [Get Event Images](https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2/#event-images-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier for the event. |
