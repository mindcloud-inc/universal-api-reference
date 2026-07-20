# Add Guide to Collection with Dubble

Adds a guide to a collection in Dubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/guides/:guideId/collections/:collectionId`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Add Guide to Collection](https://dubble.readme.io/reference/addguidetocollection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | The ID of the collection |
| `guideId` | path | `string` | yes | The ID of the guide |
