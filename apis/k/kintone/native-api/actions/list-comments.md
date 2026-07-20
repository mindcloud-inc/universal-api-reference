# List Comments with Kintone

Retrieves comments from a Kintone record.

## Endpoint

- **Method:** `GET`
- **Path:** `/record/comments.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [List Comments](https://kintone.dev/en/docs/kintone/rest-api/records/get-comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `record` | query | `number` | yes | The Kintone record ID. |
| `order` | query | `string` | no | Comment sort order. Use asc for oldest first or desc for newest first. |
| `offset` | query | `number` | no | Number of comments to skip before returning results. |
| `limit` | query | `number` | no | Maximum number of comments to return. |
