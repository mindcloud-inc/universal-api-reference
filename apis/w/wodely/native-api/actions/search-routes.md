# Search Routes with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/routes/search`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Search Routes](https://app.wodely.com/doc/api-documentation.html#get-routes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDateTime` | body | `string` | yes | UTC ISO 8601 start of the route search window. |
| `endDateTime` | body | `string` | yes | UTC ISO 8601 end of the route search window. |
| `routeId` | body | `string` | no | Optional route identifier to fetch a specific route. |
| `statusId` | body | `string` | no | Optional route status filter. |
