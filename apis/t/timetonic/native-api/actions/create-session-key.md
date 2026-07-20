# Create Session Key with Timetonic

Creates a session key in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Create Session Key](https://timetonic.com/live/api.php?doc=#createSesskey-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `o_u` | body | `string` | yes | OAuth user ID returned by User Login. |
| `u_c` | body | `string` | yes | TimeTonic user ID for the session. |
| `oauthkey` | body | `string` | yes | OAuth key returned by User Login. |
| `restrictions` | body | `string` | no | Optional session restrictions string. |
