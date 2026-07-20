# Update Team with Pingdom

## Endpoint

- **Method:** `PUT`
- **Path:** `/alerting/teams/:teamid`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Update Team](https://docs.pingdom.com/api/#tag/Teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `number` | yes | Identifier of the team. |
| `name` | body | `string` | yes | Team name. |
| `member_ids[]` | body | `array<number>` | yes | Contact identifiers that belong to the team. |
