# eWeLink: Native API Reference

A consolidated summary of eWeLink's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md
- **API base URL:** `https://{region}-apia.coolkit.cc`

## Authentication

### OAuth2

Connect an eWeLink account with CoolKit OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://c2ccdn.coolkit.cc/oauth/index.html to approve access.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens.

[Official authentication documentation](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/OAuth2.0.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Group](actions/add-group.md) | `POST /v2/device/group` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Add GSM Device](actions/add-gsm-device.md) | `POST /v2/device/add-gsm` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Add Home](actions/add-home.md) | `POST /v2/family` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Add Room](actions/add-room.md) | `POST /v2/family/room` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Add WiFi Device](actions/add-wifi-device.md) | `POST /v2/device/add` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Batch Update Device Or Group Status](actions/batch-update-device-or-group-status.md) | `POST /v2/device/thing/batch-status` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Cancel Sharing](actions/cancel-sharing.md) | `DELETE /v2/device/share` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Device Tags](actions/change-device-tags.md) | `POST /v2/device/tags` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Group Name](actions/change-group-name.md) | `PUT /v2/device/group` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Group Status](actions/change-group-status.md) | `POST /v2/device/group/status` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Home Name](actions/change-home-name.md) | `PUT /v2/family` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Password](actions/change-password.md) | `POST /v2/user/change-pwd` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Room Name](actions/change-room-name.md) | `PUT /v2/family/room` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Change Sharing Permission](actions/change-sharing-permission.md) | `POST /v2/device/share/permit` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Clean Device Operating History](actions/clean-device-operating-history.md) | `DELETE /v2/device/history` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Delete Device](actions/delete-device.md) | `DELETE /v2/device` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Delete Group](actions/delete-group.md) | `DELETE /v2/device/group` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Delete Home](actions/delete-home.md) | `DELETE /v2/family` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Delete Room](actions/delete-room.md) | `DELETE /v2/family/room` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Dispatch Service](actions/dispatch-service.md) | `GET https://{{credentials.authorizeRequest.region}}-dispa.coolkit.cc/dispatch/app` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Device Operating History](actions/get-device-operating-history.md) | `GET /v2/device/history` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Device Or Group Status](actions/get-device-or-group-status.md) | `GET /v2/device/thing/status` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Device OTA Update Information](actions/get-device-ota-update-information.md) | `POST /v2/device/ota/query` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Group List](actions/get-group-list.md) | `GET /v2/device/group` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Homes And Rooms](actions/get-homes-and-rooms.md) | `GET /v2/family` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Messages](actions/get-messages.md) | `GET /v2/message/read` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Specified Things](actions/get-specified-things.md) | `POST /v2/device/thing` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get Thing List](actions/get-thing-list.md) | `GET /v2/device/thing` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Get User Information](actions/get-user-information.md) | `GET /v2/user/profile` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [HomePage](actions/homepage.md) | `POST /v2/homepage` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Logout](actions/logout.md) | `DELETE /v2/user/logout` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Move Things](actions/move-things.md) | `POST /v2/family/room/thing` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Share Devices](actions/share-devices.md) | `POST /v2/device/share` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Sort Rooms](actions/sort-rooms.md) | `POST /v2/family/room/index` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Sort Things In Home](actions/sort-things-in-home.md) | `POST /v2/family/thing/sort` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Switch Current Home](actions/switch-current-home.md) | `POST /v2/family/current` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Update Device Name Or Room](actions/update-device-name-or-room.md) | `POST /v2/device/update-info` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Update Device Or Group Status](actions/update-device-or-group-status.md) | `POST /v2/device/thing/status` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Update Group Device List](actions/update-group-device-list.md) | `POST /v2/device/group/update` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
| [Update User Information](actions/update-user-information.md) | `POST /v2/user/profile` | [docs](https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md) |
