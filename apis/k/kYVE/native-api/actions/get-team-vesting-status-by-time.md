# Get Team Vesting Status By Time with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/team/v1beta1/team_vesting_status_by_time/{id}/{time}`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [Get Team Vesting Status By Time](https://api.kyve.network/static/openapi.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Team vesting account ID. |
| `time` | path | `string` | yes | Unix timestamp to calculate vesting progress at. |
