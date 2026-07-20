# Add Keyword with Raven Tools

Creates a new keyword for a domain in Raven Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://api.raventools.com`
- **Official documentation:** [Add Keyword](https://api.raventools.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | The domain to add the keyword to. |
| `keyword` | query | `string` | yes | The keyword to add. |
