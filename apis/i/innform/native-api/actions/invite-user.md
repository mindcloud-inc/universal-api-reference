# Invite User with Innform

Invites a new user to Innform.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Invite User](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for the invited user. |
| `groups[]` | body | `array<string>` | no | Optional list of group names. Send multiple values as a array. |
| `mobile` | body | `string` | no | Optional mobile number. |
| `name` | body | `string` | yes | Full name for the invited user. |
| `property` | body | `string` | no | Property name to assign to the user. |
| `role` | body | `string` | no | Role value: admin or student. Accepted values: `0`, `1`. |
