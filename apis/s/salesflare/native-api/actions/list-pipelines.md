# List Pipelines with Salesflare

## Endpoint

- **Method:** `GET`
- **Path:** `pipelines`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [List Pipelines](https://api.salesflare.com/docs#/Pipelines/getPipelines)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_by` | query | `string` | no | Sort expression for pipelines. |
| `search` | query | `string` | no | Free-text search across pipelines. |
