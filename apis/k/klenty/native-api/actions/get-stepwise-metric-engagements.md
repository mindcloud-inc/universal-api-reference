# Get Stepwise Metric Engagements with Klenty

Retrieves stepwise metric engagements from Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/stepWiseEngagements`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Get Stepwise Metric Engagements](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_52fc68a546)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cadenceName` | body | `string` | yes | Cadence name to report stepwise metrics for. |
| `endDate` | body | `string` | yes | End date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |
| `startDate` | body | `string` | yes | Start date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |
