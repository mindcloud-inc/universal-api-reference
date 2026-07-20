# List Field Allowed Values with Tricentis qTest

Retrieves allowed field values from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/settings/{objectType}/fields/{fieldId}/allowed-values`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [List Field Allowed Values](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `objectType` | path | `string` | yes | Object type, such as releases, builds, requirements, test-cases, test-steps, defects, or test-runs. |
| `fieldId` | path | `number` | yes | ID of the field. |
