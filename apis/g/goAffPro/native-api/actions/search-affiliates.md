# Search Affiliates with GoAffPro

Finds affiliates in GoAffPro by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/affiliates/search`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Search Affiliates](https://api.goaffpro.com/docs/admin/)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `in[]` | query | `array<string>` | yes | Affiliate fields to search in. |
| `keyword` | query | `string` | yes | Search keyword. |
| `fields[]` | query | `array<string>` | yes | Fields to include in the returned affiliate records. |
