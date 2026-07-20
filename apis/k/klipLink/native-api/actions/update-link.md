# Update Link with KlipLink

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/links/:short_url`
- **Base URL:** `https://api.klipl.ink`
- **Official documentation:** [Update Link](https://docs.klipl.ink/api/links/update-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | path | `string` | yes | The short URL identifier, for example klipl.ink/example. |
| `destination_url` | body | `string` | no | Optional new destination URL for the link. |
| `title` | body | `string` | no | Optional new title for the link. |
