# List Notes with Clio Manage

Retrieves notes from your Clio Manage account.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [List Notes](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Notes/operation/Note%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | yes | The Clio note type to return. Accepted values: `Contact`, `Matter`. |
