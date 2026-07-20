# Check Can Validate with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/query/v1beta1/can_validate/{pool_id}/{pool_address}`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [Check Can Validate](https://api.kyve.network/static/openapi.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pool_id` | path | `string` | yes | Pool ID to check validation against. |
| `pool_address` | path | `string` | yes | Pool address to validate. |
