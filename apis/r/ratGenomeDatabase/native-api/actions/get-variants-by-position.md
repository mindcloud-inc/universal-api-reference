# Get Variants By Position with Rat Genome Database

## Endpoint

- **Method:** `GET`
- **Path:** `/variants/:chr/:start/:stop/:mapKey`
- **Base URL:** `https://rest.rgd.mcw.edu/rgdws`
- **Official documentation:** [Get Variants By Position](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chr` | path | `string` | yes |
| `start` | path | `number` | yes |
| `stop` | path | `number` | yes |
| `mapKey` | path | `number` | yes |
