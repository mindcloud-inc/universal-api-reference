# List Platform Post History with Ayrshare

Retrieves post history for a platform from Ayrshare.

## Endpoint

- **Method:** `GET`
- **Path:** `/history/:platform`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [List Platform Post History](https://www.ayrshare.com/docs/apis/history/history-platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | path | `string` | yes | Social network platform, such as instagram, facebook, twitter, linkedin, or youtube. Accepted values: `bluesky`, `facebook`, `gmb`, `instagram`, `linkedin`, `pinterest`, `reddit`, `snapchat`, `telegram`, `threads`, `tiktok`, `twitter`, `youtube`. |
