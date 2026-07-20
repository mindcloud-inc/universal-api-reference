# Create Template with Pingueen

## Endpoint

- **Method:** `POST`
- **Path:** `/user/templates`
- **Base URL:** `https://api.pingueen.it/ext/v2/{businessname}`
- **Official documentation:** [Create Template](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | Template category such as UTILITY or MARKETING. |
| `components[]` | body | `array<object>` | yes | Template components array. |
| `language` | body | `string` | yes | ISO 639-1 language code. |
| `name` | body | `string` | yes | Unique lowercase template name with underscores. |
