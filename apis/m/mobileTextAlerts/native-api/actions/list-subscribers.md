# List Subscribers with Mobile Text Alerts

Retrieves subscribers from Mobile Text Alerts.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [List Subscribers](https://developers.mobile-text-alerts.com/api-reference/subscribers#get-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `pageSize` | query | `number` | no | Number of subscribers per page. |
| `query` | query | `string` | no | Search by subscriber name, number, or email. |
