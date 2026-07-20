# Get Test Run with Tricentis qTest

Retrieves a test run from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/test-runs/{testRunId}`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [Get Test Run](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `testRunId` | path | `number` | yes | ID of the Test Run. |
