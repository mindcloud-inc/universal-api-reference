# Get Member Statistics with Referral Rock

Retrieves member sharing and reward statistics from Referral Rock.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/memberstats/getsingle`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Get Member Statistics](https://api.referralrock.com/Help/Api/GET-api-memberstats-getsingle_query_timePeriod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | A member email address, ID, external ID, or referral code. |
| `timePeriod` | query | `string` | yes | One of All, MonthToDate, LastMonth, Last7Days, or Last30Days. |
