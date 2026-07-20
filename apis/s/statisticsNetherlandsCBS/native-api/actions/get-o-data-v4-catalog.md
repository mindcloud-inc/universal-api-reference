# Get OData V4 Catalog with Statistics Netherlands CBS

Retrieves an OData V4 catalog from Statistics Netherlands CBS.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/Catalogs('{{identifier}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Catalog](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | CBS OData v4 catalog identifier, such as CBS. |
