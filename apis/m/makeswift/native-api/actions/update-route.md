# Update Route with Makeswift

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/routes/:routeIdOrPathname`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Update Route](https://docs.makeswift.com/developer/reference/api/routes/update-route)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routeIdOrPathname` | path | `string` | yes | Route ID or pathname to update. |
| `siteId` | query | `string` | yes | The site ID containing the route. |
| `skipValidation` | query | `boolean` | no | Skip route conflict validation when true. |
| `pathname` | body | `string` | no | Updated pathname for the route. |
