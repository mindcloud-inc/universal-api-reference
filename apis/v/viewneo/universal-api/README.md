# <img src="https://images.mindcloud.co/apps/icons/viewneo_1775499698031.png" alt="Viewneo logo" width="28" height="28"> Viewneo: Universal API

Manage digital signage content, playlists, devices, and account data in Viewneo using the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/viewneo/latest
- **Category:** Website & App Building / CMS
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.viewneo.com
- **Vendor API docs:** https://cloud.viewneo.com/doc/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves the current account details from Viewneo. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves the current company details from Viewneo. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices for the current account in Viewneo. |
| [List Devices For Analytics](actions/list-devices-for-analytics.md) | GET | Retrieves devices for analytics from Viewneo. |

### Device Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Device Group](actions/create-device-group.md) | POST | Creates a new device group in Viewneo. |
| [Delete Device Group](actions/delete-device-group.md) | DELETE | Deletes an existing device group from Viewneo. |
| [Get Device Group](actions/get-device-group.md) | GET | Retrieves a device group from Viewneo. |
| [List Device Groups](actions/list-device-groups.md) | GET | Retrieves all device groups from Viewneo. |
| [Update Device Group](actions/update-device-group.md) | PUT | Updates an existing device group in Viewneo. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Check Website Embeddability](actions/check-website-embeddability.md) | GET | Checks website embeddability for a media file in Viewneo. |
| [Copy Multiple Media Files](actions/copy-multiple-media-files.md) | POST | Copies multiple media files in Viewneo. |
| [Create Folder](actions/create-folder.md) | POST | Creates a new media folder in Viewneo. |
| [Create Playlist](actions/create-playlist.md) | POST | Creates a new playlist in Viewneo. |
| [Create Website Media File](actions/create-website-media-file.md) | POST | Creates a new website media file in Viewneo. |
| [Delete Media File](actions/delete-media-file.md) | DELETE | Deletes an existing media file from Viewneo. |
| [Delete Playlist](actions/delete-playlist.md) | DELETE | Deletes an existing playlist from Viewneo. |
| [Get Media File or Folder Contents](actions/get-media-file-or-folder-contents.md) | GET | Retrieves a media file or folder contents from Viewneo. |
| [Get Media Thumbnail](actions/get-media-thumbnail.md) | GET | Retrieves a media thumbnail from Viewneo. |
| [Get Media Tree](actions/get-media-tree.md) | GET | Retrieves the media tree from Viewneo. |
| [Get Playlist](actions/get-playlist.md) | GET | Retrieves a specific playlist from Viewneo. |
| [List Media Files](actions/list-media-files.md) | GET | Retrieves media files and folders from Viewneo. |
| [List Playlists](actions/list-playlists.md) | GET | Retrieves playlists for the current account in Viewneo. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates for the current account in Viewneo. |
| [List Website Media Files](actions/list-website-media-files.md) | GET | Retrieves website media files from Viewneo. |
| [Move Multiple Media Files](actions/move-multiple-media-files.md) | PUT | Moves multiple media files in Viewneo. |
| [Rename Media File](actions/rename-media-file.md) | PUT | Updates a media file name in Viewneo. |
| [Update Playlist](actions/update-playlist.md) | PUT | Updates an existing playlist in Viewneo. |
| [Upload Media File](actions/upload-media-file.md) | POST | Uploads a media file to Viewneo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users for the current account in Viewneo. |

