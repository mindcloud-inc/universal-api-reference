# Delete Database Record with Bika.ai

Deletes a database record from Bika.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/spaces/:spaceId/resources/databases/:nodeId/records/:recordId`
- **Base URL:** `https://bika.ai/api/openapi/bika/v1`
- **Official documentation:** [Delete Database Record](https://bika.ai/help/guide/developer/openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Bika.ai workspace/space ID. |
| `nodeId` | path | `string` | yes | Database node ID. In Bika.ai, the node ID is equivalent to the database ID for database resources. |
| `recordId` | path | `string` | yes | Record ID to delete. |
