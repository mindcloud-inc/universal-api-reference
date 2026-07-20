# Get API Usage with ZeroBounce

Retrieves API usage metrics from ZeroBounce by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/getapiusage`
- **Base URL:** `https://api.zerobounce.net`
- **Official documentation:** [Get API Usage](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-get-api-usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date in yyyy-mm-dd format. |
| `end_date` | query | `string` | yes | End date in yyyy-mm-dd format. |
