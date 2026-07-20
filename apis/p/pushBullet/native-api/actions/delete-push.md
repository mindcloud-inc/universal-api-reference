# Delete Push with Pushbullet

Deletes an existing push from Pushbullet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pushes/:push_iden`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Delete Push](https://docs.pushbullet.com/v8/#pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `push_iden` | path | `string` | yes | Push identifier to delete. |
