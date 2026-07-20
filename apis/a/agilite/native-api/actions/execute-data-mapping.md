# Execute Data Mapping with Agilite

Executes a data mapping profile in Agilite by profile key.

## Endpoint

- **Method:** `POST`
- **Path:** `/datamappings/execute`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Execute Data Mapping](https://docs.agilite.io/reference/execute-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile-key` | query | `string` | yes | Data mapping profile key. |
| `data` | body | `object` | no | Optional JSON body values used by the data mapping profile. |
