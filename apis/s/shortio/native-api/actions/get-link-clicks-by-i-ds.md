# Get Link Clicks By IDs with Short.io

Retrieves link clicks from Short.io by link IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `https://statistics.short.io/statistics/domain/:domainId/link_clicks`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Get Link Clicks By IDs](https://developers.short.io/v1.2/reference/getdomaindomainidlink_clicks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainId` | path | `number` | yes | Domain ID. |
| `ids` | query | `string` | no | Optional link ID selector. Pass one link ID or a comma-separated list of link IDs. |
