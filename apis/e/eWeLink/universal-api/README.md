# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-17-as-14_1776448475244.png" alt="eWeLink logo" width="28" height="28"> eWeLink: Universal API

Control and manage eWeLink / SONOFF smart-home devices, homes, rooms, groups, sharing, messages, and device status through the CoolKit eWeLink API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eWeLink/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ewelink.cc/
- **Vendor API docs:** https://github.com/CoolKit-Technologies/eWeLink-API/blob/main/en/APICenterV2.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Information](actions/get-user-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Clean Device Operating History](actions/clean-device-operating-history.md) | DELETE | Deletes device operating history from eWeLink. |
| [Get Device Operating History](actions/get-device-operating-history.md) | GET | Retrieves device operating history from eWeLink. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Add GSM Device](actions/add-gsm-device.md) | POST | Creates a new GSM device in eWeLink. |
| [Add WiFi Device](actions/add-wifi-device.md) | POST | Creates a new Wi-Fi device in eWeLink. |
| [Batch Update Device Or Group Status](actions/batch-update-device-or-group-status.md) | PUT | Updates device or group statuses in batch in eWeLink. |
| [Change Device Tags](actions/change-device-tags.md) | PUT | Updates device tags in eWeLink. |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes an existing device from eWeLink. |
| [Get Device Or Group Status](actions/get-device-or-group-status.md) | GET | Retrieves device or group status from eWeLink. |
| [Get Device OTA Update Information](actions/get-device-ota-update-information.md) | GET | Retrieves device OTA update information from eWeLink. |
| [Get Specified Things](actions/get-specified-things.md) | GET | Retrieves specified things from eWeLink. |
| [Get Thing List](actions/get-thing-list.md) | GET | Retrieves things from eWeLink. |
| [HomePage](actions/homepage.md) | GET | Retrieves homepage device data from eWeLink. |
| [Move Things](actions/move-things.md) | PUT | Updates room assignments for things in eWeLink. |
| [Sort Things In Home](actions/sort-things-in-home.md) | PUT | Updates thing order in an eWeLink home. |
| [Update Device Name Or Room](actions/update-device-name-or-room.md) | PUT | Updates a device name or room in eWeLink. |
| [Update Device Or Group Status](actions/update-device-or-group-status.md) | PUT | Updates device or group status in eWeLink. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Group](actions/add-group.md) | POST | Creates a new group in eWeLink. |
| [Change Group Name](actions/change-group-name.md) | PUT | Updates a group name in eWeLink. |
| [Change Group Status](actions/change-group-status.md) | PUT | Updates group status in eWeLink. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from eWeLink. |
| [Get Group List](actions/get-group-list.md) | GET | Retrieves groups from eWeLink. |
| [Update Group Device List](actions/update-group-device-list.md) | PUT | Updates a group device list in eWeLink. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Add Home](actions/add-home.md) | POST | Creates a new home in eWeLink. |
| [Add Room](actions/add-room.md) | POST | Creates a new room in eWeLink. |
| [Change Home Name](actions/change-home-name.md) | PUT | Updates a home name in eWeLink. |
| [Change Room Name](actions/change-room-name.md) | PUT | Updates a room name in eWeLink. |
| [Delete Home](actions/delete-home.md) | DELETE | Deletes an existing home from eWeLink. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from eWeLink. |
| [Get Homes And Rooms](actions/get-homes-and-rooms.md) | GET | Retrieves homes and rooms from eWeLink. |
| [Sort Rooms](actions/sort-rooms.md) | PUT | Updates room order in eWeLink. |
| [Switch Current Home](actions/switch-current-home.md) | PUT | Updates the current home in eWeLink. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Messages](actions/get-messages.md) | GET | Retrieves messages from eWeLink. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Sharing](actions/cancel-sharing.md) | DELETE | Deletes a sharing permission from eWeLink. |
| [Change Sharing Permission](actions/change-sharing-permission.md) | PUT | Updates a sharing permission in eWeLink. |
| [Share Devices](actions/share-devices.md) | POST | Creates a device sharing entry in eWeLink. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Dispatch Service](actions/dispatch-service.md) | GET | Retrieves dispatch service information from eWeLink. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Logout](actions/logout.md) | DELETE | Ends the current user session in eWeLink. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Change Password](actions/change-password.md) | PUT | Updates the user password in eWeLink. |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves user information from eWeLink. |
| [Update User Information](actions/update-user-information.md) | PUT | Updates user information in eWeLink. |

