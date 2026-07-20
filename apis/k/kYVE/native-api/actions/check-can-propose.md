# Check Can Propose with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/query/v1beta1/can_propose/{pool_id}/{staker}/{proposer}/{from_index}`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [Check Can Propose](https://api.kyve.network/static/openapi.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pool_id` | path | `string` | yes | Pool ID to check proposal against. |
| `staker` | path | `string` | yes | Staker address. |
| `proposer` | path | `string` | yes | Proposer address. |
| `from_index` | path | `string` | yes | Bundle index to propose from. |
