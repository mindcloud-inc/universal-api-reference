# List Items with Qlik

Retrieves items from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/items`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Items](https://qlik.dev/apis/rest/items/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Optional search query for items. |
