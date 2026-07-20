# Upload File V2 with ImageKit.io

Uploads a file to ImageKit.io using Upload API v2.

## Endpoint

- **Method:** `POST`
- **Path:** `https://upload.imagekit.io/api/v2/files/upload`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Upload File V2](https://imagekit.io/docs/api-reference/upload-file/upload-file-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | — |
| `fileName` | body | `string` | yes | — |
| `folder` | body | `string` | no | — |
| `useUniqueFileName` | body | `boolean` | no | — |
| `isPrivateFile` | body | `boolean` | no | — |
| `tags` | body | `list<string>` | no | Send multiple values as a array. |
| `customCoordinates` | body | `string` | no | — |
| `responseFields` | body | `list<string>` | no | Send multiple values as a array. |
| `webhookUrl` | body | `string` | no | — |
| `overwriteFile` | body | `boolean` | no | — |
| `overwriteAITags` | body | `boolean` | no | — |
| `overwriteTags` | body | `boolean` | no | — |
| `overwriteCustomMetadata` | body | `boolean` | no | — |
| `customMetadata` | body | `string` | no | — |
| `extensions` | body | `string` | no | — |
| `transformation` | body | `string` | no | — |
| `checks` | body | `string` | no | — |
| `token` | body | `string` | no | — |
