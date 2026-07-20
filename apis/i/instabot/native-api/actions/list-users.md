# List Users with Instabot

Retrieves users from Instabot.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [List Users](https://docs.instabot.io/docs/serverapi-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | User type selector. Instabot documents `all` for both anonymous and registered users. |
