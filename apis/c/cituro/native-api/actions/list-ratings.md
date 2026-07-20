# List Ratings with Cituro

Retrieves a list of ratings from Cituro.

## Endpoint

- **Method:** `GET`
- **Path:** `/ratings/:accountNumber`
- **Base URL:** `https://app.cituro.com/api`
- **Official documentation:** [List Ratings](https://www.cituro.com/help/bewertungen-auf-webseite-einbinden)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountNumber` | path | `string` | yes | The Cituro account number used in the ratings endpoint path. |
| `limit` | query | `number` | no | Maximum number of ratings to return. |
| `sort` | query | `string` | no | Sort expression such as -createdAt for newest first. |
