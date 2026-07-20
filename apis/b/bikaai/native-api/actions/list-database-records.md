# List Database Records with Bika.ai

Retrieves database records from Bika.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/resources/databases/:nodeId/records`
- **Base URL:** `https://bika.ai/api/openapi/bika/v1`
- **Official documentation:** [List Database Records](https://bika.ai/help/guide/developer/openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Bika.ai workspace/space ID. |
| `nodeId` | path | `string` | yes | Database node ID. In Bika.ai, the node ID is equivalent to the database ID for database resources. |
