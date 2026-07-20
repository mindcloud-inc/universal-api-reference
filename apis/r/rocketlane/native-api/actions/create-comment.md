# Create Comment with Rocketlane

Creates a comment in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/comments`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Create Comment](https://developer.rocketlane.com/reference/create-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeFields` | query | `string` | no | — |
| `content` | body | `string` | yes | Content of the comment |
| `source` | body | `object` | yes | Source associated with the comment |
| `attachments` | body | `list<object>` | no | List of attachments associated with the comment |
| `private` | body | `boolean` | no | — |
