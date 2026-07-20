# List Test Suites with Tricentis qTest

Retrieves test suites from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/test-suites`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [List Test Suites](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
