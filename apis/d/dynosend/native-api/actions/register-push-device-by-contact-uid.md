# Register Push Device by Contact UID with Dynosend

Registers a push device in Dynosend by contact UID.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.dynosend.com/device/register`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Register Push Device by Contact UID](https://docs.dynosend.com/a-21-firebase-cloud-messaging-fcm-setup-for-push-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | The Dynosend mobile push project ID. |
| `contact_uid` | body | `string` | yes | The UID of the Dynosend contact that owns the device. |
| `fcm_token` | body | `string` | yes | The Firebase Cloud Messaging device token to register. |
