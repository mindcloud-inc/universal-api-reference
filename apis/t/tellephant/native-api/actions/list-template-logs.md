# List template logs with Tellephant

Retrieves template message logs from Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/user/logs`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [List template logs](https://app.tellephant.com/api-documentation#get-template-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `string` | yes | Start date in DD-MM-YYYY format. |
| `end_date` | body | `string` | yes | End date in DD-MM-YYYY format. |
| `page` | query | `number` | no | Optional page number for paginated log results. |
