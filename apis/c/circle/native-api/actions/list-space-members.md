# List Space Members with Circle

Retrieves space membership records from Circle.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/v2/space_members`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [List Space Members](https://api.circle.so/apis/admin-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | query | `list<number>` | yes | Space ID |
