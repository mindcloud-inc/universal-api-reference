# Get Document Content with Webling

## Endpoint

- **Method:** `GET`
- **Path:** `/document/:id/file/:filename.:extension`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [Get Document Content](https://demo.webling.ch/api/1#document-document-content-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Document ID to download. |
| `filename` | path | `string` | yes | File name without extension. |
| `extension` | path | `string` | yes | File extension. |
