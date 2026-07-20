# Viewneo: Native API Reference

A consolidated summary of Viewneo's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://cloud.viewneo.com/doc/api
- **OpenAPI specification:** https://cloud.viewneo.com/docs
- **API base URL:** `https://cloud.viewneo.com/api/v1.0`

## Authentication

### Personal Access Token

Authenticate Viewneo requests with a personal access token from the API Plugin dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.viewneo.com/en/developers-guide/viewneo-api/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Website Embeddability](actions/check-website-embeddability.md) | `GET /mediafile/:id/check-x-frame-options` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.check-x-frame-options) |
| [Copy Multiple Media Files](actions/copy-multiple-media-files.md) | `POST /mediafile/copy/:targetId` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.copy.multiple) |
| [Create Device Group](actions/create-device-group.md) | `POST /devicegroup` | [docs](https://cloud.viewneo.com/doc/api#/DeviceGroup/api.deviceGroup.store) |
| [Create Folder](actions/create-folder.md) | `POST /mediafile` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.store.directory) |
| [Create Playlist](actions/create-playlist.md) | `POST /playlist` | [docs](https://cloud.viewneo.com/doc/api#/Playlist/api.playlist.store) |
| [Create Website Media File](actions/create-website-media-file.md) | `POST /mediafile` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.store.website) |
| [Delete Device Group](actions/delete-device-group.md) | `DELETE /devicegroup/:id` | [docs](https://cloud.viewneo.com/doc/api#/DeviceGroup/api.deviceGroup.delete) |
| [Delete Media File](actions/delete-media-file.md) | `DELETE /mediafile/:id` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.delete) |
| [Delete Playlist](actions/delete-playlist.md) | `DELETE /playlist/:id` | [docs](https://cloud.viewneo.com/doc/api#/Playlist/api.playlist.delete) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://cloud.viewneo.com/doc/api#/Account/get_account) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://cloud.viewneo.com/doc/api#/Company/api.company.index) |
| [Get Device Group](actions/get-device-group.md) | `GET /devicegroup/:id` | [docs](https://cloud.viewneo.com/doc/api#/DeviceGroup/api.deviceGroup.show) |
| [Get Media File or Folder Contents](actions/get-media-file-or-folder-contents.md) | `GET /mediafile/:id` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.show) |
| [Get Media Thumbnail](actions/get-media-thumbnail.md) | `GET /mediafile/:id/thumbnail` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.thumbnail) |
| [Get Media Tree](actions/get-media-tree.md) | `GET /treeview` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.tree) |
| [Get Playlist](actions/get-playlist.md) | `GET /playlist/:id` | [docs](https://cloud.viewneo.com/doc/api#/Playlist/api.playlist.show) |
| [List Device Groups](actions/list-device-groups.md) | `GET /devicegroup` | [docs](https://cloud.viewneo.com/doc/api#/DeviceGroup/api.deviceGroup.index) |
| [List Devices](actions/list-devices.md) | `GET /device` | [docs](https://cloud.viewneo.com/doc/api#/Device/api.device.index) |
| [List Devices For Analytics](actions/list-devices-for-analytics.md) | `GET /devices-for-analytics` | [docs](https://cloud.viewneo.com/doc/api#/Device/api.device.getDevicesForAnalytics) |
| [List Media Files](actions/list-media-files.md) | `GET /mediafile` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.index) |
| [List Playlists](actions/list-playlists.md) | `GET /playlist` | [docs](https://cloud.viewneo.com/doc/api#/Playlist/api.playlist.index) |
| [List Templates](actions/list-templates.md) | `GET /template` | [docs](https://cloud.viewneo.com/doc/api#/Template/api.template.index) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://cloud.viewneo.com/doc/api#/User/api.user.index) |
| [List Website Media Files](actions/list-website-media-files.md) | `GET /mediafile/websites` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.getAllWebsiteMediaFiles) |
| [Move Multiple Media Files](actions/move-multiple-media-files.md) | `POST /mediafile/move/:targetId` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.move.multiple) |
| [Rename Media File](actions/rename-media-file.md) | `POST /mediafile/:id` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.update.rename) |
| [Update Device Group](actions/update-device-group.md) | `POST /devicegroup/:id` | [docs](https://cloud.viewneo.com/doc/api#/DeviceGroup/api.deviceGroup.update) |
| [Update Playlist](actions/update-playlist.md) | `POST /playlist/:id` | [docs](https://cloud.viewneo.com/doc/api#/Playlist/api.playlist.update) |
| [Upload Media File](actions/upload-media-file.md) | `POST /mediafile` | [docs](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.store.physical) |
