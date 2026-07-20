# List User Achievements with Bonusly

Retrieves achievements for a Bonusly user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/achievements`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [List User Achievements](https://docs.bonus.ly/reference/achievements-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bonusly user ID whose achievements to list. |
