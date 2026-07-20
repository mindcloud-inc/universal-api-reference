# Delete Route with Makeswift

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/routes/:routeIdOrPathname`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Delete Route](https://docs.makeswift.com/developer/reference/api/routes/delete-route)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routeIdOrPathname` | path | `string` | yes | Route ID or pathname to delete. |
| `siteId` | query | `string` | yes | The site ID containing the route. |
