# Filter Groups with Qlik

Finds groups in Qlik by advanced filter query.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/groups/actions/filter`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Filter Groups](https://qlik.dev/apis/rest/groups/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `string` | yes | SCIM filter expression for matching groups. |
