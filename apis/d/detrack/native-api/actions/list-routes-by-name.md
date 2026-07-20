# List Routes By Name with Detrack

Finds routes in Detrack by route name and date.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/routes`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [List Routes By Name](https://detrackapiv2.docs.apiary.io/#reference/routes/retrieve-route-by-name/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Route date in YYYY-MM-DD format. |
| `name` | query | `string` | no | Route name to retrieve. |
