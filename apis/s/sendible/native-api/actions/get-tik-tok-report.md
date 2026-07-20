# Get TikTok Report with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `0.2/tw/tiktok/report`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Get TikTok Report](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `number` | yes | TikTok account ID. |
| `end` | query | `string` | yes | Report end date. |
| `module` | query | `string` | yes | TikTok report module, such as ActivityOverview or Audience. |
| `start` | query | `string` | yes | Report start date. |
| `timezoneOffset` | query | `number` | yes | Timezone offset in minutes. |
