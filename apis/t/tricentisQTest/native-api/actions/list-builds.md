# List Builds with Tricentis qTest

Retrieves available builds from Tricentis qTest.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/builds`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [List Builds](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `releaseId` | query | `number` | yes | ID of the parent Release. |
