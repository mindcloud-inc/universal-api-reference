# Delete Organization Secret with Port API AI

Deletes an organization secret from Port.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organization/secrets/:secret_name`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Delete Organization Secret](https://docs.port.io/api-reference/delete-an-organization-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secret_name` | path | `string` | yes | The Port organization secret name. |
