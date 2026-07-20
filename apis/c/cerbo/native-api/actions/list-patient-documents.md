# List Patient Documents with Cerbo

Retrieves patient documents from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/documents`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Documents](https://docs.cer.bo/#tag/Patient-Documents/operation/listPatientDocuments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `folder` | query | `string` | no | (optional) String (folder name). Limits results to a specific folder or "tab." |
