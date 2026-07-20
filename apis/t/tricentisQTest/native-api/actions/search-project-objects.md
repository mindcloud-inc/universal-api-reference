# Search Project Objects with Tricentis qTest

Finds project objects in Tricentis qTest by query criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{projectId}/search`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [Search Project Objects](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `body` | body | `object` | yes | Project object search body including object_type and query clauses. |
