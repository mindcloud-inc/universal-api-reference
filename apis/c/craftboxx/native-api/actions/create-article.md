# Create Article with Craftboxx

Creates an article in Craftboxx.

## Endpoint

- **Method:** `POST`
- **Path:** `articles`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Create Article](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | no | The article currency. |
| `name` | body | `string` | yes | The article name. |
| `unit_price` | body | `number` | no | The article unit price. |
