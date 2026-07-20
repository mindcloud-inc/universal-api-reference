# Get Gene By Symbol with Rat Genome Database

## Endpoint

- **Method:** `GET`
- **Path:** `/genes/:symbol/:speciesTypeKey`
- **Base URL:** `https://rest.rgd.mcw.edu/rgdws`
- **Official documentation:** [Get Gene By Symbol](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `symbol` | path | `string` | yes |
| `speciesTypeKey` | path | `number` | yes |
