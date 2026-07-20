# Search Clients with Whautomate

Finds matching clients in Whautomate.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/clients`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Search Clients](https://help.whautomate.com/product-guides/whautomate-rest-api/clients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endDate` | query | `date` | no |
| `primaryLocationId` | query | `string` | no |
| `searchText` | query | `string` | no |
| `startDate` | query | `date` | no |
| `tags` | query | `string` | no |
