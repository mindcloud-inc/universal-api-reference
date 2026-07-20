# Create Story Version with Storydoc

Creates a new story version in Storydoc.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/versions`
- **Base URL:** `https://api.storydoc.com`
- **Official documentation:** [Create Story Version](https://docs.storydoc.com/operation/operation-createstoryversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storyId` | body | `string` | yes | The ID of the story template to version. |
| `senderEmail` | body | `string` | yes | Email of the sender. It must exist in the Storydoc organization. |
| `daysToExpire` | body | `number` | no | Number of days until the version expires. |
| `data` | body | `object` | yes | Storydoc version data object. It must include at least a title field. |
