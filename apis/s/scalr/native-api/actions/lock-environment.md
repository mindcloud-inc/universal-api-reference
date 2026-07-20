# Lock Environment with Scalr

Locks an environment in Scalr.

## Endpoint

- **Method:** `POST`
- **Path:** `/environments/:environment/actions/lock`
- **Base URL:** `https://mindcloud.scalr.io/api/iacp/v3`
- **Official documentation:** [Lock Environment](https://docs.scalr.io/reference/lock_environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment` | path | `string` | yes | Scalr environment ID. |
| `reason` | body | `string` | no | Reason for locking the environment. |
