# Update Article with Craftboxx

Updates an article in Craftboxx.

## Endpoint

- **Method:** `PUT`
- **Path:** `articles/:articleId`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Update Article](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleId` | path | `number` | yes | The Craftboxx article ID. |
| `currency` | body | `string` | no | The article currency. |
| `name` | body | `string` | no | The article name. |
| `unit_price` | body | `number` | no | The article unit price. |
