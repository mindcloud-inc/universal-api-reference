# Update Promotion with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/promotions/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Promotion](https://developers.swell.is/backend-api/promotions/update-a-promotion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell promotion ID. |
| `discounts[]` | body | `array<object>` | yes | Promotion discount rules. |
| `name` | body | `string` | no | The promotion name. |
| `active` | body | `boolean` | no | Whether the promotion is active. |
| `date_start` | body | `date` | no | The promotion start timestamp. |
| `date_end` | body | `date` | no | The promotion end timestamp. |
| `description` | body | `string` | no | The promotion description. |
