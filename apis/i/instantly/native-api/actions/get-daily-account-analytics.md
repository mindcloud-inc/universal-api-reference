# Get Daily Account Analytics with Instantly

Get analytics for the specified sender accounts. Useful for tracking daily sending activity across your accounts.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/accounts/analytics/daily`
- **Base URL:** `https://api.instantly.ai`
- **API:** rest
- **Official documentation:** [Get Daily Account Analytics](https://developer.instantly.ai/api/v2/account/getdailyaccountanalytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | no | Start date for the analytics period, YYYY-MM-DD. |
| `end_date` | query | `date` | no | End date for the analytics period, YYYY-MM-DD. |
| `emails[]` | query | `array<string>` | no | Email accounts to filter by. Send multiple values as a array. |
