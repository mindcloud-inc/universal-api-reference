# Update Recipient with Trolley

Updates an existing recipient in Trolley.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/recipients/:id`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Update Recipient](https://developers.trolley.com/api/#update-a-recipient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
