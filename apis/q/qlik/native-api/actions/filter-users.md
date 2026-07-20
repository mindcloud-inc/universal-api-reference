# Filter Users with Qlik

Finds users in Qlik by advanced filter query.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/users/actions/filter`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Filter Users](https://qlik.dev/apis/rest/users/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `string` | yes | SCIM filter expression for matching users. |
