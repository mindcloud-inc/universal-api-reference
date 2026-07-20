# List change log with RealFaviconGenerator

## Endpoint

- **Method:** `GET`
- **Path:** `/change-log`
- **Base URL:** `https://realfavicongenerator.net/api`
- **Official documentation:** [List change log](https://realfavicongenerator.net/developers/change-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `string` | no | Only return changes after this existing RealFaviconGenerator version, such as 0.5. |
| `format` | query | `list` | no | Human-readable description format returned by the API. Accepted values: `html`, `markdown`. |
