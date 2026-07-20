# Get User Groups with Request Tracker (RT)

Retrieves a user's groups from Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `user/:userId/groups`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Get User Groups](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#User-Memberships)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The RT user ID or username. |
