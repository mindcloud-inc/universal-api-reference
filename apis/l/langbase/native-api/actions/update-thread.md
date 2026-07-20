# Update Thread with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/threads/:threadId`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Update Thread](https://langbase.com/docs/api-reference/threads/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | path | `string` | yes | Thread ID to update. |
| `metadata` | body | `object` | no | Metadata object to merge into the thread. |
