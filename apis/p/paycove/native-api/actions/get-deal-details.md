# Get Deal Details with Paycove

Retrieves a deal from Paycove.

## Endpoint

- **Method:** `GET`
- **Path:** `deals/:id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Get Deal Details](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_field_keys[]` | query | `array<string>` | no | Array of custom field keys to include in the response. |
| `id` | path | `string` | yes | Paycove deal id. |
| `scope[]` | query | `array<string>` | no | Array of relations to include, such as contact or organization. |
