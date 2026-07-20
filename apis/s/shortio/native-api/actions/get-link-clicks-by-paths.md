# Get Link Clicks By Paths with Short.io

Retrieves link clicks from Short.io by paths.

## Endpoint

- **Method:** `POST`
- **Path:** `https://statistics.short.io/statistics/domain/:domainId/link_clicks`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Get Link Clicks By Paths](https://developers.short.io/v1.2/reference/postdomaindomainidlink_clicks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainId` | path | `number` | yes | Domain ID. |
| `paths[]` | body | `array<string>` | no | Optional link path selector list. |
