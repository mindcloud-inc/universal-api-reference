# Get Shared Link Metadata with Dropbox

Retrieves metadata for a Dropbox shared link.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/get_shared_link_metadata`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Get Shared Link Metadata](https://www.dropbox.com/developers/documentation/http/documentation#sharing-get_shared_link_metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Shared link URL to inspect. |
| `path` | body | `string` | no | Optional relative path inside the shared link. |
| `link_password` | body | `string` | no | Password for a password-protected shared link. |
