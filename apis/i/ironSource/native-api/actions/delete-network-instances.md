# Delete Network Instances with ironSource

Deletes existing network instances from ironSource.

## Endpoint

- **Method:** `DELETE`
- **Path:** `levelPlay/network/instances/v4/:appKey`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Delete Network Instances](https://docs.unity.com/en-us/grow/levelplay/platform/api/instances-api-v4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | path | `string` | no | Application key as seen on the LevelPlay platform. |
| `ids` | body | `string` | no | Array of instance IDs to delete. |
