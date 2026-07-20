# List Prospects By List with Klenty

Retrieves prospects from a Klenty list.

## Endpoint

- **Method:** `GET`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [List Prospects By List](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_82aa5a533c)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listName` | query | `string` | yes | List name to filter prospects by. |
| `start` | query | `number` | no | Page number to start from. |
| `limit` | query | `number` | no | Maximum number of prospects to return. |
