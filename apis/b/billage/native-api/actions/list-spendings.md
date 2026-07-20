# List Spendings with Billage

Retrieves spending records from Billage by code or date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/spendings`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [List Spendings](https://app.getbillage.com/api/documentation.html#/Spendings/spendingsByParameters)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search spendings |
| `ref` | query | `string` | no | Reference code |
| `serie` | query | `string` | no | Serie |
| `account` | query | `string` | no | Account |
| `colour` | query | `string` | no | Colour name |
| `date-from` | query | `date` | no | Date from (yyyy-MM-dd) |
| `date-to` | query | `date` | no | Date to (yyyy-MM-dd) |
| `owner` | query | `string` | no | Spending owner |
| `state` | query | `string` | no | Spending state |
| `category` | query | `string` | no | Spending category |
| `tags[]` | query | `array<string>` | no | Spending tags |
| `summarized` | query | `boolean` | no | Summarized |
