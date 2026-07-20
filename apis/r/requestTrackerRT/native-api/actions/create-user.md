# Create User with Request Tracker (RT)

Creates a new user in Request Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `user`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Create User](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EmailAddress` | body | `string` | no | Primary email address for the user. |
| `Name` | body | `string` | yes | RT username for the new user. |
| `Privileged` | body | `boolean` | no | Set to true to create a privileged RT user. |
| `RealName` | body | `string` | no | Display name for the user. |
