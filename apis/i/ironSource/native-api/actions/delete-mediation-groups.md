# Delete Mediation Groups with ironSource

Deletes existing mediation groups from ironSource.

## Endpoint

- **Method:** `DELETE`
- **Path:** `levelPlay/groups/v4/:appKey`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Delete Mediation Groups](https://docs.unity.com/en-us/grow/levelplay/platform/api/groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appKey` | path | `string` | no | Application key as seen on the LevelPlay platform. |
| `ids` | body | `string` | no | Array of mediation group IDs to delete. |
