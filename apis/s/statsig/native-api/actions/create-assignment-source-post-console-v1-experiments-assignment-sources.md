# Create Assignment Source with Statsig

Creates an assignment source in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/assignment_sources`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Assignment Source](https://docs.statsig.com/api-reference/experiments/create-assignment-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `isVerified` | body | `boolean` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `sql` | body | `string` | yes | Request body field. |
| `timestampColumn` | body | `string` | yes | Request body field. |
| `experimentIDColumn` | body | `string` | yes | Request body field. |
| `groupIDColumn` | body | `string` | yes | Request body field. |
| `groupNameColumn` | body | `string` | no | Request body field. |
| `idTypeMapping` | body | `list` | yes | Request body field. |
| `isReadOnly` | body | `boolean` | no | Request body field. |
| `owner` | body | `object` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `scheduledReloadHour` | body | `number` | no | Request body field. |
| `dryRun` | body | `boolean` | no | Request body field. |
