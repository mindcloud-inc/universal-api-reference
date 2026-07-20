# Update Return Portal with Webshipper

Updates a return portal in Webshipper.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/return_portals/:id`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Update Return Portal](https://docs.webshipper.io/#return_portals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The return portal ID. |
| `data.id` | body | `string` | yes | Repeat the ID value for the JSON:API request body. |
| `data.attributes.name` | body | `string` | no | Updated portal name. |
