# Search Meeting Content with IceCubes

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [Search Meeting Content](https://icecubes.app/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search query across meeting content. |
| `content_type` | query | `string` | no | Filter by content type. |
| `speaker` | query | `string` | no | Filter by speaker name. |
| `tag` | query | `string` | no | Filter by tag name. |
