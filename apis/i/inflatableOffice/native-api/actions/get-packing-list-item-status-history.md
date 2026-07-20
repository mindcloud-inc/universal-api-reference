# Get Packing List Item Status History with InflatableOffice

Retrieves packing list item status history from InflatableOffice.

## Endpoint

- **Method:** `GET`
- **Path:** `/packinglists`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [Get Packing List Item Status History](https://rental.software/support/knowledge-base/article/api-packing-lists-retrieve-details-or-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | query | `number` | yes | Lead ID to retrieve packing list history for. |
| `rental_id` | query | `number` | yes | Rental ID to retrieve packing list history for. |
