# Find Clients with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/find_clients`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Find Clients](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `object` | yes | Search expression object for Salebot variable lookup. |
| `search_in` | body | `string` | no | Set to order to search deal variables instead of client variables. |
| `include_all` | body | `boolean` | no | Require all query predicates to match. |
