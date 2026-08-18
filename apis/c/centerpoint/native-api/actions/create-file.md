# Create File with Centerpoint

## Endpoint

- **Method:** `POST`
- **Path:** `files`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create File](https://api.centerpointconnect.io/centerpoint/files)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `object` | yes |
| `data.attributes` | body | `object` | yes |
| `data.attributes.url` | body | `string` | yes |
| `data.attributes.title` | body | `string` | yes |
| `data.attributes.description` | body | `string` | no |
