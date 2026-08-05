# List Account Summaries with Google Analytics

## Endpoint

- **Method:** `GET`
- **Path:** `https://analyticsadmin.googleapis.com/v1beta/accountSummaries`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [List Account Summaries](https://developers.google.com/analytics/devguides/config/admin/v1/rest/v1beta/accountSummaries/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | no | Maximum account summaries to return (up to 200) |
| `pageToken` | query | `string` | no | Token from a previous response |
