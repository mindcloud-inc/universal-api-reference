# List Skills with Anthropic

Retrieves skills from the Anthropic account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/skills`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Skills](https://platform.claude.com/docs/en/api/beta/skills/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of skills to return. |
| `page` | query | `string` | no | Opaque page token for pagination. |
| `source` | query | `string` | no | Optional source filter (for example user or system). |
