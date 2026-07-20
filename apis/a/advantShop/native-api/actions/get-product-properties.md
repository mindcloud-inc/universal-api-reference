# Get Product Properties with AdvantShop

Retrieves product properties from AdvantShop.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/{id}/properties`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Product Properties](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Product identifier from AdvantShop. |
| `type` | query | `list` | no | Optional property view type, such as inDetails or inBriefDescription. Accepted values: `0`, `1`. |
