# Get Member Achievements with Habitica

Retrieves a member's achievements from Habitica.

## Endpoint

- **Method:** `GET`
- **Path:** `/members/:memberId/achievements`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Get Member Achievements](https://habitica.com/apidoc/#api-Member-GetMemberAchievements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memberId` | path | `string` | yes | The Habitica member ID. |
