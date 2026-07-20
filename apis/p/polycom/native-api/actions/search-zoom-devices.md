# Search Zoom Devices with Polycom

Searches Poly Lens devices whose active application is Zoom.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [Search Zoom Devices](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.params.sort.fields[0].name` | body | `string` | yes | Sort field name. |
| `variables.params.pageSize` | body | `number` | no | Maximum number of devices to return. |
| `variables.params.nextToken` | body | `string` | no | Opaque token for the next page of results. |
