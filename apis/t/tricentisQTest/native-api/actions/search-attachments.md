# Search Attachments with Tricentis qTest

Finds attachments in Tricentis qTest by object criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/attachments`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [Search Attachments](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `type` | query | `string` | yes | Artifact type to search attachments for, such as releases, builds, requirements, test-cases, test-logs, test-steps, or defects. |
