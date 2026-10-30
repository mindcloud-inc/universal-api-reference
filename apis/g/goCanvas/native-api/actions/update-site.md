# Update Site with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sites/:siteId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Update Site](https://api.gocanvas.com/api/v3/docs#update-a-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `number` | yes | Identifier of the site to update. |
| `name` | body | `string` | yes | Name of the site; marked required by the PATCH table. |
| `address` | body | `string` | no | Address of the site. |
| `city` | body | `string` | no | City of the site. |
| `state` | body | `string` | no | State of the site. |
| `zip_code` | body | `string` | no | Postal code of the site. |
| `country` | body | `string` | no | Two-letter country abbreviation. |
| `code` | body | `string` | no | Alphanumeric code uniquely identifying the site. |
| `customer_id` | body | `number` | no | Identifier of a customer associated with the company. |
