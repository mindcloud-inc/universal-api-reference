# Submit Event Data with Absinthe

Submits event data to an Absinthe registered event.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/{event_id}/data`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Submit Event Data](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_id` | path | `string` | yes |
| `account_id` | body | `string` | yes |
| `identity_type` | body | `string` | yes |
| `amount` | body | `number` | yes |
