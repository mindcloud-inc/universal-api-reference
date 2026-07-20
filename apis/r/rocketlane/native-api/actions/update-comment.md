# Update Comment with Rocketlane

Updates a comment in Rocketlane.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.0/comments/:commentId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Update Comment](https://developer.rocketlane.com/reference/update-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `number` | yes | The ID of the comment object |
| `includeFields` | query | `string` | no | — |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `commentId` | body | `number` | no | Comment ID |
| `content` | body | `string` | no | Updated comment content |
| `private` | body | `boolean` | no | — |
