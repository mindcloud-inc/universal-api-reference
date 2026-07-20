# Search Teams and Zoom Devices with Polycom

Searches Poly Lens devices whose active application is Microsoft or Zoom.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [Search Teams and Zoom Devices](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Hidden GraphQL document for the Teams-and-Zoom device search. |
| `variables.params.filter.OR[0].contains` | body | `string` | yes | Hidden first provider filter value. |
| `variables.params.filter.OR[1].contains` | body | `string` | yes | Hidden second provider filter value. |
| `variables.params.sort.fields[0].name` | body | `string` | yes | Sort field name. |
| `variables.params.pageSize` | body | `number` | no | Maximum number of devices to return. |
| `variables.params.nextToken` | body | `string` | no | Opaque token for the next page of results. |
