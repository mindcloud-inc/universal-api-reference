# Get DNC List Items with Saleshandy

## Endpoint

- **Method:** `GET`
- **Path:** `/dnc/[:dncListId]`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Get DNC List Items](https://developer.saleshandy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dncListId` | path | `string` | yes | DNC list ID to fetch items for. |
| `search` | query | `string` | no | Optional DNC item search string within the selected list. |
| `type` | query | `string` | yes | DNC item type to filter by. |
