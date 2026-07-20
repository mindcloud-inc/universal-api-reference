# Get Annotations For Term with Rat Genome Database

## Endpoint

- **Method:** `GET`
- **Path:** `/annotations/:accId/:speciesTypeKey/:includeChildren`
- **Base URL:** `https://rest.rgd.mcw.edu/rgdws`
- **Official documentation:** [Get Annotations For Term](https://rest.rgd.mcw.edu/rgdws/rgd-api-docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accId` | path | `string` | yes |
| `speciesTypeKey` | path | `number` | yes |
| `includeChildren` | path | `boolean` | yes |
