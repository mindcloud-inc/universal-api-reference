# List Forms with FillFaster

Retrieves a list of active forms from FillFaster.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/getFormsList`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [List Forms](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Sort order. Use desc or asc. |
| `page` | query | `number` | no | Results page number. FillFaster defaults to 1. |
| `sort` | query | `string` | no | Sort field. FillFaster documents created as the default. |
| `wid` | query | `string` | no | Optional workspace id when you need to scope the forms list. |
