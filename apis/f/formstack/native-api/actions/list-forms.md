# List Forms with Formstack

Retrieves forms from Formstack with filtering and sorting.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [List Forms](https://developers.formstack.com/reference/getformslist-1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search by form name. |
| `folder` | query | `number` | no | Filter forms by folder ID. |
