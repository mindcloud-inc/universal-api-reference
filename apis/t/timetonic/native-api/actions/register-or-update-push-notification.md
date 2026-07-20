# Register Or Update Push Notification with Timetonic

Creates or updates a push registration in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Register Or Update Push Notification](https://timetonic.com/live/api.php?doc=#updatePushId-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceID` | body | `string` | yes | Device identifier to register or update. |
| `deviceType` | body | `string` | yes | Push device type. Docs list gcm_rid, gcm_nk, ios_dt, ios_dt_v2, bb_dt, or win_uri. |
| `active` | body | `string` | yes | Whether the push registration is active. |
| `registrationID` | body | `string` | yes | Push registration token. |
| `projectID` | body | `string` | yes | Push project identifier. |
