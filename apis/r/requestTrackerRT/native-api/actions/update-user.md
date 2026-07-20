# Update User with Request Tracker (RT)

Updates an existing user in Request Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `user/:userId`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Update User](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Disabled` | body | `boolean` | no | Set to true to disable the user. |
| `EmailAddress` | body | `string` | no | Updated primary email address for the user. |
| `Organization` | body | `string` | no | Updated organization name for the user. |
| `Privileged` | body | `boolean` | no | Set to true to mark the user as privileged. |
| `RealName` | body | `string` | no | Updated display name for the user. |
| `userId` | path | `string` | yes | The RT user ID or username. |
