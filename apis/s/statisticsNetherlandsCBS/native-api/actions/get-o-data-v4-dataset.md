# Get OData V4 Dataset with Statistics Netherlands CBS

Retrieves an OData V4 dataset from Statistics Netherlands CBS.

## Endpoint

- **Method:** `GET`
- **Path:** `https://datasets.cbs.nl/odata/v1/CBS/Datasets('{{identifier}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get OData V4 Dataset](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | CBS OData v4 dataset identifier, such as 00372. |
