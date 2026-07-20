# Update Mediation Groups with ironSource

Updates existing mediation groups in ironSource.

## Endpoint

- **Method:** `PUT`
- **Path:** `levelPlay/groups/v4/:appKey`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Update Mediation Groups](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | path | `string` | no | Application key as seen on the LevelPlay platform. |
| `groups` | body | `string` | no | Array of mediation group objects to update. |
