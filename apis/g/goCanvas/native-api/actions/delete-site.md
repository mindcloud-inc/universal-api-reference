# Delete Site with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sites/:siteId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Site](https://api.gocanvas.com/api/v3/docs#delete-a-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | — |
| `hard_delete` | query | `boolean` | no | Permanently deletes the site when true. Omit for soft delete. |
