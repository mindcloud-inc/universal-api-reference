# Create Shared Link with Dropbox

Creates a shared link in Dropbox, or returns an existing link.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/create_shared_link_with_settings`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Create Shared Link](https://www.dropbox.com/developers/documentation/http/documentation#sharing-create_shared_link_with_settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | — |
| `settings.allow_download` | body | `boolean` | no | Whether the new shared link should allow downloads. |
