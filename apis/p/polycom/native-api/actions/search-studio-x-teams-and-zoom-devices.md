# Search Studio X Teams and Zoom Devices with Polycom

Searches Studio X devices in Poly Lens running Teams or Zoom.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [Search Studio X Teams and Zoom Devices](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Hidden GraphQL document for the Studio X Teams-and-Zoom device search. |
| `variables.params.filter.AND[0].OR[0].contains` | body | `string` | yes | First application filter value. |
| `variables.params.filter.AND[0].OR[1].contains` | body | `string` | yes | Second application filter value. |
| `variables.params.filter.AND[1].contains` | body | `string` | yes | Hardware model filter value. |
| `variables.params.sort.fields[0].name` | body | `string` | yes | Sort field name. |
| `variables.params.pageSize` | body | `number` | no | Maximum number of devices to return. |
| `variables.params.nextToken` | body | `string` | no | Opaque token for the next page of results. |
