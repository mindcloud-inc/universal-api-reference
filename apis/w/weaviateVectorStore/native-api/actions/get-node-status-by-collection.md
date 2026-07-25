# Get node status by collection with Weaviate Vector Store

Retrieves node status by collection from Weaviate.

## Endpoint

- **Method:** `GET`
- **Path:** `/nodes/:className`
- **Base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`
- **Official documentation:** [Get node status by collection](https://docs.weaviate.io/weaviate/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classname` | path | `string` | yes | The name of the collection (class) for which to retrieve node status. |
| `shardName` | query | `string` | no | — |
| `output` | query | `string` | no | Controls the verbosity of the output, possible values are: `minimal`, `verbose`. Defaults to `minimal`. |
