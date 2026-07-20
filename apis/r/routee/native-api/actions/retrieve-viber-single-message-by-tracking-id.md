# Retrieve Viber Single Message by Tracking Id with Routee

Retrieves Viber single message by tracking id from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/viber/tracking/:trackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve Viber Single Message by Tracking Id](https://docs.routee.net/reference/retrieve-single-viber-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | The tracking Id of the Viber single message. |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
| `sort` | query | `number` | no | The field name that will be used to sort the results. |
