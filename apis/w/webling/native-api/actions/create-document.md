# Create Document with Webling

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [Create Document](https://demo.webling.ch/api/1#document-document-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties.title` | body | `string` | yes | Document title, including the filename and extension Webling should store. |
| `parents` | body | `number` | yes | Documentgroup ID that should own the new document. |
| `properties.content` | body | `string` | yes | Base64-encoded file content for the new document. |
