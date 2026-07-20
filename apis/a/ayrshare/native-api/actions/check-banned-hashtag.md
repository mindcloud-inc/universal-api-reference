# Check Banned Hashtag with Ayrshare

Checks whether a hashtag is banned in Ayrshare.

## Endpoint

- **Method:** `GET`
- **Path:** `/hashtags/banned`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Check Banned Hashtag](https://www.ayrshare.com/docs/apis/hashtags/check-hashtags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hashtag` | query | `string` | yes | Hashtag to check, including the leading # when available. |
