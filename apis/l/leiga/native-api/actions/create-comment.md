# Create Comment with Leiga

Creates a new comment in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/comment/add`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Create Comment](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741893.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentModule` | body | `string` | yes | Comment Module (.eg. issue) |
| `linkId` | body | `number` | yes | Link ID |
| `content` | body | `string` | yes | Comment Content |
