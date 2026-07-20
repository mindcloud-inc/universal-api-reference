# Check Can Vote with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/query/v1beta1/can_vote/{pool_id}/{staker}/{voter}/{storage_id}`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [Check Can Vote](https://api.kyve.network/static/openapi.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pool_id` | path | `string` | yes | Pool ID to check voting against. |
| `staker` | path | `string` | yes | Staker address. |
| `voter` | path | `string` | yes | Voter address. |
| `storage_id` | path | `string` | yes | Storage ID of the bundle. |
