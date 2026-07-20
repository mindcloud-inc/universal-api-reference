# Remove Keyword with Raven Tools

Deletes a keyword from a domain in Raven Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://api.raventools.com`
- **Official documentation:** [Remove Keyword](https://api.raventools.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | The domain to remove the keyword from. |
| `keyword` | query | `string` | yes | The keyword to remove. |
