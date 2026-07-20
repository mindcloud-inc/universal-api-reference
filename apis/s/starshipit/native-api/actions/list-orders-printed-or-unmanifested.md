# List Orders (Printed or Unmanifested) with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/shipments`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [List Orders (Printed or Unmanifested)](https://api-docs.starshipit.com/#bc249299-e979-4003-becc-27ba61dcf214)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since_created_date` | query | `date` | no | Show shipments created after date in UTC (date-time in RFC3339 format) |
| `status` | query | `string` | no | The status of the shipments to return |
| `limit` | query | `string` | no | Amount of results (default: 50) (maximum: 250) |
| `page` | query | `string` | no | Page to show (default: 1) |
