# Create Database Record with Bika.ai

Creates a database record in Bika.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:spaceId/resources/databases/:nodeId/records`
- **Base URL:** `https://bika.ai/api/openapi/bika/v1`
- **Official documentation:** [Create Database Record](https://bika.ai/help/guide/developer/openapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Bika.ai workspace/space ID. |
| `nodeId` | path | `string` | yes | Database node ID. In Bika.ai, the node ID is equivalent to the database ID for database resources. |
| `cells` | body | `object` | yes | Object whose keys are field names and values are the cell values to write. |
