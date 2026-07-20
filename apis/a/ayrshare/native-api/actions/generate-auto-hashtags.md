# Generate Auto Hashtags with Ayrshare

Adds relevant hashtags to a post in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/hashtags/auto`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Generate Auto Hashtags](https://www.ayrshare.com/docs/apis/hashtags/auto-hashtags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post` | body | `string` | yes | Post text to generate relevant hashtags for. |
