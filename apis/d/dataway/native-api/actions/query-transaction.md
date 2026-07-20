# Query Transaction with Dataway

Retrieves transaction details from Dataway by client reference.

## Endpoint

- **Method:** `POST`
- **Path:** `/query-transaction`
- **Base URL:** `https://datawayapp.com/vendor`
- **Official documentation:** [Query Transaction](https://documenter.getpostman.com/view/421216/UV5Ukz4U)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | Client reference to query. |
