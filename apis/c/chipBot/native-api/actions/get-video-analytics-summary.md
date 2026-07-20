# Get Video Analytics Summary with ChipBot

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId/reporting/summary`
- **Base URL:** `https://getchipbot.com`
- **Official documentation:** [Get Video Analytics Summary](https://getchipbot.com/api-docs/video-exp/video-analytics-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | The report end timestamp in ISO-8601 format. |
| `startDate` | query | `string` | yes | The report start timestamp in ISO-8601 format. |
| `tz` | query | `string` | yes | The timezone offset used by the report window, for example -06:00. |
| `videoExpId` | path | `string` | yes | The video experience identifier, for example videxp_xxx. |
