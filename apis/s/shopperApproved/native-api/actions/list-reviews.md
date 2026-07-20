# List Reviews with Shopper Approved

Retrieves reviews from Shopper Approved.

## Endpoint

- **Method:** `GET`
- **Path:** `/reviews/:siteid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [List Reviews](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | The first date in YYYY-MM-DD format. |
| `to` | query | `date` | no | The last date in YYYY-MM-DD format. |
| `rating` | query | `string` | no | Comma-separated star ratings to include. |
| `sort` | query | `string` | no | How the reviews should be sorted. |
| `full_name` | query | `number` | no | Whether to include the reviewer's full last name. |
| `removed` | query | `number` | no | Whether to include removed reviews. |
| `test` | query | `boolean` | no | Whether to include reviews marked as test or possible spam. |
