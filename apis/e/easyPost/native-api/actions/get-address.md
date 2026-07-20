# Get Address with EasyPost

Retrieves details for an address from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/addresses/:id`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Address](https://docs.easypost.com/docs/addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Address ID, beginning with adr_. |
