# Get multiple portfolios with Asana

Retrieves portfolios from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `portfolios`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple portfolios](https://developers.asana.com/reference/getportfolios)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `workspace` | query | `string` | yes | Asana workspace parameter. |
| `owner` | query | `string` | no | Asana owner parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
