# List Linked Artifacts with Tricentis qTest

Retrieves linked artifacts from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/linked-artifacts`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [List Linked Artifacts](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `type` | query | `string` | yes | Artifact type such as releases, builds, requirements, test-cases, test-runs, test-logs, test-steps, or defects. |
