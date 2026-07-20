# Update Shared Link Settings with Dropbox

Updates shared link settings in Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/modify_shared_link_settings`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Update Shared Link Settings](https://www.dropbox.com/developers/documentation/http/documentation#sharing-modify_shared_link_settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | — |
| `settings.allow_download` | body | `boolean` | yes | Whether the shared link should allow downloads after the update. |
