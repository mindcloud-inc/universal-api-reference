# Get Sending Reports with SMSEdge

Retrieves SMS sending reports from SMSEdge.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/sending/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Get Sending Reports](https://developers.smsedge.io/reference/reports-sending)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | no | Filter results by minimum date in YYYY-MM-DD format. |
| `date_to` | query | `string` | no | Filter results by maximum date in YYYY-MM-DD format. |
| `limit` | query | `number` | no | Maximum items to return per request. |
| `offset` | query | `number` | no | Number of items to skip before returning results. |
| `status` | query | `string` | no | Filter by SMS sending status: sent, waiting, failed. |
