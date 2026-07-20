# Save Variables with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/save_variables`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Save Variables](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | no | Existing Salebot client ID. |
| `variables` | body | `object` | yes | Key-value map of Salebot variables to save. |
| `clients[]` | body | `array<number>` | no | Optional array of client IDs for bulk variable assignment. |
