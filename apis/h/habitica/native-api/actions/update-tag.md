# Update Tag with Habitica

Updates an existing tag in Habitica.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:tagId`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Update Tag](https://habitica.com/apidoc/#api-Tag-UpdateTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `string` | yes | The Habitica tag ID. |
| `name` | body | `string` | yes | The updated tag name. |
