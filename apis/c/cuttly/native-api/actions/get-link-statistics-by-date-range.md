# Get Link Statistics By Date Range with Cutt.ly

Retrieves date-range click statistics for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Get Link Statistics By Date Range](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stats` | query | `string` | yes | The short link whose analytics you want to fetch. |
| `date_from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `date_to` | query | `string` | no | End date in YYYY-MM-DD format. |
