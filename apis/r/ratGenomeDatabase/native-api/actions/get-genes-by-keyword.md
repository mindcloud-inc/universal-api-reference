# Get Genes By Keyword with Rat Genome Database

## Endpoint

- **Method:** `GET`
- **Path:** `/genes/keyword/:keyword/:speciesTypeKey`
- **Base URL:** `https://rest.rgd.mcw.edu/rgdws`
- **Official documentation:** [Get Genes By Keyword](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keyword` | path | `string` | yes |
| `speciesTypeKey` | path | `number` | yes |
