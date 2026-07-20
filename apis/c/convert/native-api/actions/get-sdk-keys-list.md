# List SDK Keys with Convert

Retrieves SDK keys from a Convert project.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/projects/:project_id/sdk-keys`
- **Base URL:** `https://api.convert.com/api/v2`
- **Official documentation:** [List SDK Keys](https://api.convert.com/doc/v2/#tag/SDK-Keys/operation/getSdkKeysList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Convert project ID. |
