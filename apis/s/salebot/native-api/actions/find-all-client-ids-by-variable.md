# Find All Client IDs by Variable with Salebot

## Endpoint

- **Method:** `GET`
- **Path:** `/find_all_client_id_by_var`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Find All Client IDs by Variable](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `var` | query | `string` | yes | Variable name to search. |
| `val` | query | `string` | yes | Variable value to match. |
