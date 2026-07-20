# Get Defect Comment with Tricentis qTest

Retrieves a defect comment from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/defects/{idOrKey}/comments/{commentId}`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [Get Defect Comment](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `idOrKey` | path | `string` | yes | PID or ID of the Defect. |
| `commentId` | path | `number` | yes | ID of the comment. |
