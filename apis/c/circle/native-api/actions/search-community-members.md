# Search Community Members with Circle

Finds community members in Circle by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/v2/community_members/search`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Search Community Members](https://api.circle.so/apis/admin-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email of the community member |
