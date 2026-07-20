# Update Link with Dub

Updates a link in Dub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/links/:linkId`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Update Link](https://dub.co/docs/api-reference/links/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | Dub link ID to update. |
| `title` | body | `string` | no | Updated link title. |
| `archived` | body | `boolean` | no | Archive or unarchive the link. |
