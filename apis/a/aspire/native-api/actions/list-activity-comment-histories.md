# List Activity Comment Histories with Aspire

Retrieves activity comment histories from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `ActivityCommentHistories`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Activity Comment Histories](https://cloud-api.youraspire.com/swagger/index.html#/ActivityCommentHistories/ActivityCommentHistories_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
