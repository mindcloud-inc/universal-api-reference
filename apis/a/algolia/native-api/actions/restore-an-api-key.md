# Restore an API Key with Algolia

Restores a deleted API key in Algolia.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/keys/:key/restore`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Restore an API Key](https://www.algolia.com/doc/rest-api/search/restore-api-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | API key to restore. |
