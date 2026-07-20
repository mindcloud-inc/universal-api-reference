# Create Connect Campaign with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Create Connect Campaign](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Campaign title. |
| `url` | body | `string` | no | Optional LinkedIn search URL used as the campaign source. |
| `content.shortNote` | body | `string` | no | Optional short connection note, up to 175 characters. Maximum length: 175. |
| `content.longNote` | body | `string` | no | Optional long connection note, up to 275 characters. Maximum length: 275. |
| `content.message1` | body | `string` | yes | First follow-up message. |
| `content.message2` | body | `string` | no | Optional second follow-up message. |
| `content.message3` | body | `string` | no | Optional third follow-up message. |
