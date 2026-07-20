# Get Refund with EasyPost

Retrieves details for a refund from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/refunds/:id`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Refund](https://docs.easypost.com/docs/refunds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Refund ID, beginning with rfnd_. |
