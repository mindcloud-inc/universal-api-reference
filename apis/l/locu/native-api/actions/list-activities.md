# List Activities with Locu

Retrieves a paginated list of session activities from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/activities`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Activities](https://locu.app/api/docs#tag/sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderBy` | query | `string` | no | Sort field. Allowed values: updatedAt or createdAt. |
| `order` | query | `string` | no | Sort direction. Allowed values: asc or desc. |
| `taskId` | query | `string` | no | Filter activities by task ID. |
| `sessionId` | query | `string` | no | Filter activities by session ID. |
