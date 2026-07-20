# Search Tickets with Zoho Desk

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/search`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Search Tickets](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Search.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Search for an exact Zoho Desk ticket ID. |
| `departmentId` | query | `list<number>` | no | — |
| `channel` | query | `list<string>` | no | — |
| `createdTimeRange` | query | `string` | no | — |
