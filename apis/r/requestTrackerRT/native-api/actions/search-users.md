# Search Users with Request Tracker (RT)

Finds users in Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `users`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Search Users](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Users)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated RT fields to include in each user result. |
| `query` | query | `string` | yes | JSON search array for RT users, serialized as a string. |
