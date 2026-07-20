# List Integrations with DeployHQ

Retrieves project integrations from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/integrations`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [List Integrations](https://api.deployhq.com/docs#tag/Integrations/operation/listProjectIntegrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
