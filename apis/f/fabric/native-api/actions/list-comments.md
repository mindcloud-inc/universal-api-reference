# List Comments with Fabric

Retrieves comments for a resource from Fabric.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/{resourceId}/comments`
- **Base URL:** `https://api.fabric.so`
- **Official documentation:** [List Comments](https://developers.fabric.so/api-reference/tag/comments/get/v2/resources/resourceId/comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessToken` | query | `string` | no | Access token for published-resource comments when required. |
| `limit` | query | `number` | no | Maximum number of comments to return. |
| `offset` | query | `number` | no | Number of comments to skip before returning results. |
| `resourceId` | path | `string` | yes | The Fabric resource ID for the comments to list. |
