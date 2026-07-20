# Upload File with Flatfile

Uploads a new file to Flatfile.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Upload File](https://reference.flatfile.com/api-reference/files/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | body | `string` | yes | Flatfile environment identifier. |
| `file` | body | `string` | yes | File upload payload. |
| `spaceId` | body | `string` | yes | Flatfile space identifier. |
