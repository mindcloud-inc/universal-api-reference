# Update Guide with Dubble

Updates an existing guide in Dubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/guides/:guideId`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Update Guide](https://dubble.readme.io/reference/updateguide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guideId` | path | `string` | yes | The ID of the guide |
| `title` | body | `string` | no | The title of the guide |
| `visibility` | body | `string` | no | The visibility setting for the guide |
