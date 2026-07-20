# Update summary details with api.video

Updates summary source details in api.video.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/summaries/:summaryId/source`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Update summary details](https://docs.api.video/reference/api/Summaries#update-summary-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `abstract` | body | `string` | no | A short outline of the contents of the video. |
| `summaryId` | path | `string` | yes | The unique identifier for the summary. |
| `takeaways` | body | `string` | no | Comma-separated summary takeaways. |
