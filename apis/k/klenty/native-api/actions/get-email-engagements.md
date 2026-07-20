# Get Email Engagements with Klenty

Retrieves email engagements from Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/emailEngagements`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Get Email Engagements](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_26cb69cafc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cadenceName` | body | `string` | yes | Cadence name to report email engagement metrics for. |
| `endDate` | body | `string` | yes | End date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |
| `startDate` | body | `string` | yes | Start date for the engagement window. Use yyyy-mm-dd or an ISO timestamp as documented. |
