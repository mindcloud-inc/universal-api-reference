# List Submissions with NeetoForm

Retrieves submissions for a NeetoForm form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:form_id/submissions`
- **Base URL:** `https://{workspaceSubdomain}.neetoform.com/api/external/v1`
- **Official documentation:** [List Submissions](https://apidocs.neetoform.com/api-reference/submissions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form whose submissions you want to retrieve. |
