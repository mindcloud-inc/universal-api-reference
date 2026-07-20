# List Object Fields with Tricentis qTest

Retrieves object fields from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/settings/{objectType}/fields`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [List Object Fields](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `objectType` | path | `string` | yes | Object type, such as releases, builds, requirements, test-cases, test-steps, defects, or test-runs. |
