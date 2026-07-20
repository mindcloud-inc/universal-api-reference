# Get Campaign Posts Report with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `1.0/api/campaign/report/posts`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Get Campaign Posts Report](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | query | `number` | yes | Campaign ID. |
| `orderBy` | query | `string` | no | Optional sort field. |
| `page` | query | `number` | yes | Page number. |
| `socialNetwork` | query | `string` | no | Optional social network filter. |
