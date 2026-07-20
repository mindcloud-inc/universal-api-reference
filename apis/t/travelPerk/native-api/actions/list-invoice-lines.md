# List Invoice Lines with TravelPerk

Retrieves invoice lines from TravelPerk.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/lines`
- **Base URL:** `https://api.sandbox-travelperk.com`
- **API:** rest
- **Official documentation:** [List Invoice Lines](https://developers.perk.com/docs/rest-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expense_date_gte` | query | `string` | no | Return invoice lines with an expense date on or after this date in YYYY-MM-DD format. |
| `expense_date_lte` | query | `string` | no | Return invoice lines with an expense date on or before this date in YYYY-MM-DD format. |
