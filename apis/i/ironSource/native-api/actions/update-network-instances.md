# Update Network Instances with ironSource

Updates existing network instances in ironSource.

## Endpoint

- **Method:** `PUT`
- **Path:** `levelPlay/network/instances/v4/:appKey`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Update Network Instances](https://docs.unity.com/en-us/grow/levelplay/platform/api/instances-api-v4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | path | `string` | no | Application key as seen on the LevelPlay platform. |
| `instances` | body | `string` | no | Array of network instance objects to update. |
