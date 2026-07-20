# List Comments with Leiga

Retrieves comments from Leiga for an issue.

## Endpoint

- **Method:** `POST`
- **Path:** `/comment/page`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [List Comments](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741900.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentModule` | body | `string` | yes | Comment Module (.eg. issue) |
| `linkId` | body | `number` | yes | Link ID |
| `pageNumber` | body | `number` | no | Page Number |
| `pageSize` | body | `number` | no | Page Size |
