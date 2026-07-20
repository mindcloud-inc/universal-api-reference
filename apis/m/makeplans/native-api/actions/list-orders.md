# List Orders with Makeplans

Retrieves orders from Makeplans.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [List Orders](https://developer.makeplans.com/endpoints/orders/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | no | Filter by order state: pending, confirmed, or cancelled. |
