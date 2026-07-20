# List Directory Users with WorkOS

Retrieves directory users from your WorkOS environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/directory_users`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [List Directory Users](https://workos.com/docs/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. For example, if you make a list request and receive 100 objects, ending with `"obj_123"`, your subsequent call can include `before="obj_123"` to fetch a new batch of objects before `"obj_123"`. |
| `after` | query | `string` | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. For example, if you make a list request and receive 100 objects, ending with `"obj_123"`, your subsequent call can include `after="obj_123"` to fetch a new batch of objects after `"obj_123"`. |
| `limit` | query | `number` | no | Upper limit on the number of objects to return, between `1` and `100`. |
| `order` | query | `string` | no | Order the results by the creation time. Supported values are `"asc"` (ascending), `"desc"` (descending), and `"normal"` (descending with reversed cursor semantics where `before` fetches older records and `after` fetches newer records). Defaults to descending. |
