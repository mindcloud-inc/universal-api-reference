# Create Promotion with Swell

## Endpoint

- **Method:** `POST`
- **Path:** `/promotions`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Create Promotion](https://developers.swell.is/backend-api/promotions/create-a-promotion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discounts[]` | body | `array<object>` | yes | Promotion discount rules. |
| `name` | body | `string` | no | The promotion name. |
| `active` | body | `boolean` | no | Whether the promotion is active. |
| `date_start` | body | `date` | no | The promotion start timestamp. |
| `date_end` | body | `date` | no | The promotion end timestamp. |
| `description` | body | `string` | no | The promotion description. |
