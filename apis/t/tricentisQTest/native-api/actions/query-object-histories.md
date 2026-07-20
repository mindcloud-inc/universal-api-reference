# Query Object Histories with Tricentis qTest

Finds object histories in Tricentis qTest by query criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{projectId}/histories`
- **Base URL:** `https://mindcloudapps.qtestnet.com/api/v3`
- **Official documentation:** [Query Object Histories](https://qtest-config.s3.amazonaws.com/api-docs/manager/api-manager-v3.0.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | ID of the qTest project. |
| `body` | body | `object` | yes | Object history query body including object_type and filter criteria. |
