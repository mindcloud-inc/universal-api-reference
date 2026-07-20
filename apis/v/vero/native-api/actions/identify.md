# Identify with Vero

Identifies a user profile in Vero.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/users/track`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Identify](https://help.getvero.com/api-reference/users/identify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The unique Vero user identifier to create or update. |
| `email` | body | `string` | no | The email of the customer. |
| `channels[]` | body | `array<object>` | no | Optional array of push channel descriptors for the user. |
| `data` | body | `object` | no | Optional custom properties to set on the user profile. |
