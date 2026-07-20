# Register Push Device by Email with Dynosend

Registers a push device in Dynosend by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.dynosend.com/device/register`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Register Push Device by Email](https://docs.dynosend.com/a-21-firebase-cloud-messaging-fcm-setup-for-push-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | The Dynosend mobile push project ID. |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `email` | body | `string` | yes | The email address of the contact that owns the device. |
| `fcm_token` | body | `string` | yes | The Firebase Cloud Messaging device token to register. |
