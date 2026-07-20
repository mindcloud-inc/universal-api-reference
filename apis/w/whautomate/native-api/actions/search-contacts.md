# Search Contacts with Whautomate

Finds matching contacts in Whautomate.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Search Contacts](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `channel` | query | `string` | no |
| `locationId` | query | `string` | no |
| `searchText` | query | `string` | no |
| `tags` | query | `string` | no |
