# Remove Guide from Collection with Dubble

Removes a guide from a collection in Dubble.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/guides/:guideId/collections/:collectionId`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Remove Guide from Collection](https://dubble.readme.io/reference/removeguidefromcollection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | The ID of the collection |
| `guideId` | path | `string` | yes | The ID of the guide |
