# Get Genes In Region with Rat Genome Database

## Endpoint

- **Method:** `GET`
- **Path:** `/genes/region/:chr/:start/:stop/:mapKey`
- **Base URL:** `https://rest.rgd.mcw.edu/rgdws`
- **Official documentation:** [Get Genes In Region](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chr` | path | `string` | yes |
| `start` | path | `number` | yes |
| `stop` | path | `number` | yes |
| `mapKey` | path | `number` | yes |
