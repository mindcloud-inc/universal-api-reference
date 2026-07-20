# Revoke Shared Link with Dropbox

Deletes an existing shared link from Dropbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharing/revoke_shared_link`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Revoke Shared Link](https://www.dropbox.com/developers/documentation/http/documentation#sharing-revoke_shared_link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
