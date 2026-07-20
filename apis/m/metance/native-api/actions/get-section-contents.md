# Get Section Contents with Metance

Retrieves contents from a specific Metance section.

## Endpoint

- **Method:** `GET`
- **Path:** `/contents`
- **Base URL:** `https://api.metance.com`
- **Official documentation:** [Get Section Contents](https://api.metance.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Section` | query | `string` | yes | Section name to load contents from, such as Home. |
| `Count` | query | `number` | yes | Maximum number of contents to return. |
| `PageSize` | query | `number` | yes | Page size used by the Metance contents feed. |
