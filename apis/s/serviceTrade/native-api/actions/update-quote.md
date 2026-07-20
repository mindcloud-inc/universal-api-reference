# Update Quote with ServiceTrade

Updates an existing quote in ServiceTrade.

## Endpoint

- **Method:** `PUT`
- **Path:** `quote/:quoteId`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Update Quote](https://api.servicetrade.com/api/docs#resource-quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quoteId` | path | `number` | yes | Quote to update. |
| `notes` | body | `string` | no | Updated notes for the quote. |
