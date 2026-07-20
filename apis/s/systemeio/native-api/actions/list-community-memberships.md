# List Community Memberships with Systeme.io

Retrieves the collection of community memberships from Systeme.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/community/memberships`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [List Community Memberships](https://developer.systeme.io/reference/api_communitymemberships_get_collection-1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `community` | query | `number` | no | Community ID filter |
| `contact` | query | `number` | no | Contact ID filter |
