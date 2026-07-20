# List Guided Recipes with Zapier NLA

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/search/zaps/`
- **Base URL:** `https://actions.zapier.com`
- **Official documentation:** [List Guided Recipes](https://nla.zapier.com/api/v1/dynamic/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Optional search term for guided recipe suggestions. |
| `count` | query | `number` | no | Maximum number of guided recipes to return. |
| `tags[]` | body | `array<string>` | yes | Tags used by Zapier to suggest relevant guided recipes. Send multiple values as a array. |
