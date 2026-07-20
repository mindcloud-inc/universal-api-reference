# Create Route with Makeswift

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/routes`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Create Route](https://docs.makeswift.com/developer/reference/api/routes/create-route)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | body | `string` | yes | Site ID where the route will be created. |
| `pathname` | body | `string` | yes | Route pathname (for example /new-route). |
| `skipValidation` | query | `boolean` | no | Skip route conflict validation when true. |
