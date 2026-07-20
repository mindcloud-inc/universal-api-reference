# Search Devices with Polycom

Searches Poly Lens devices and returns inventory details for each result.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.silica-prod01.io.lens.poly.com`
- **Official documentation:** [Search Devices](https://api.lens.poly.com/docs/graphql/Example%20Queries/inventory-reporting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.params.nextToken` | body | `string` | no | Opaque continuation token returned by the previous device search page. |
| `variables.params.pageSize` | body | `number` | no | Number of devices to return per page. |
