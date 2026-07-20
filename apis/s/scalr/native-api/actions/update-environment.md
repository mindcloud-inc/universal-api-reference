# Update Environment with Scalr

Updates an existing environment in Scalr.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/environments/:environment`
- **Base URL:** `https://mindcloud.scalr.io/api/iacp/v3`
- **Official documentation:** [Update Environment](https://docs.scalr.io/reference/update_environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment` | path | `string` | yes | Scalr environment ID. |
| `data.attributes.name` | body | `string` | no | Environment name. |
