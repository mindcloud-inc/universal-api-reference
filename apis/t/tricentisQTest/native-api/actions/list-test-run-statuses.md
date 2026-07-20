# List Test Run Statuses with Tricentis qTest

Retrieves test run statuses from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/test-runs/execution-statuses`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [List Test Run Statuses](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
