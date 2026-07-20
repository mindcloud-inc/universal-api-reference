# List Recently Updated Users with Instabot

Finds users in Instabot by update time.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/lastUpdated`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [List Recently Updated Users](https://docs.instabot.io/docs/serverapi-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | no | Return only users updated since this datetime. |
