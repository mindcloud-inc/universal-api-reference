# Get Genes Annotated with Rat Genome Database

## Endpoint

- **Method:** `GET`
- **Path:** `/genes/annotation/:accId/:speciesTypeKey`
- **Base URL:** `https://rest.rgd.mcw.edu/rgdws`
- **Official documentation:** [Get Genes Annotated](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accId` | path | `string` | yes |
| `speciesTypeKey` | path | `number` | yes |
