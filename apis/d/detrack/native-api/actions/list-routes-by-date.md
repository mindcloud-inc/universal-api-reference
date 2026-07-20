# List Routes By Date with Detrack

Retrieves routes from Detrack for a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/routes`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [List Routes By Date](https://detrackapiv2.docs.apiary.io/#reference/routes/retrieve-routes-by-date/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Route date in YYYY-MM-DD format. |
| `limit` | query | `string` | no | Maximum number of routes to return. |
| `page` | query | `string` | no | Page number for paginated route results. |
