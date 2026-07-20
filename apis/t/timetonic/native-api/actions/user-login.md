# User Login with Timetonic

Creates an OAuth key in Timetonic for user login.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [User Login](https://timetonic.com/live/api.php?doc=#createOauthkey-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | body | `string` | yes | TimeTonic login username or email. |
| `pwd` | body | `string` | yes | TimeTonic account password. |
| `appkey` | body | `string` | yes | App key returned by Register Application. |
