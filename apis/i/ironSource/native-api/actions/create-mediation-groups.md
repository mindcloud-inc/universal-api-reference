# Create Mediation Groups with ironSource

Creates new mediation groups in ironSource.

## Endpoint

- **Method:** `POST`
- **Path:** `levelPlay/groups/v4/:appKey`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Create Mediation Groups](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | path | `string` | no | Application key as seen on the LevelPlay platform. |
| `groups` | body | `string` | no | Array of mediation group objects to create. |
