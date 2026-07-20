# Browse Nonprofits with Every.org

Finds nonprofits in Every.org by cause.

## Endpoint

- **Method:** `GET`
- **Path:** `/browse/:cause`
- **Base URL:** `https://partners.every.org/v0.2`
- **Official documentation:** [Browse Nonprofits](https://docs.every.org/docs/endpoints/nonprofit-search#get-v02browsecause)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cause` | path | `string` | yes | Cause slug to browse. |
| `take` | query | `number` | no | Results per page. Maximum 100. |
| `page` | query | `number` | no | Page number to return. |
