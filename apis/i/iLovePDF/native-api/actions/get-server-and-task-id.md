# Get Server and Task ID with iLovePDF

Creates a task and server assignment in iLovePDF.

## Endpoint

- **Method:** `GET`
- **Path:** `/start/:tool/:region`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Get Server and Task ID](https://www.iloveapi.com/docs/api-reference#start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tool` | path | `string` | yes | iLovePDF tool key such as merge, split, compress, or pdfjpg. |
| `region` | path | `string` | yes | Processing region. Use eu for Europe or us for United States. |
