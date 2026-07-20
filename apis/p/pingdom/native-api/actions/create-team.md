# Create Team with Pingdom

## Endpoint

- **Method:** `POST`
- **Path:** `/alerting/teams`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Create Team](https://docs.pingdom.com/api/#tag/Teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Team name. |
| `member_ids[]` | body | `array<number>` | yes | Contact identifiers that belong to the team. |
