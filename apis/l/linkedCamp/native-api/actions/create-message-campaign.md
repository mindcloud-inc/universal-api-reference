# Create Message Campaign with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Create Message Campaign](https://help.linkedcamp.com/en/articles/10257445-api-create-a-new-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Campaign title. |
| `url` | body | `string` | no | Optional LinkedIn search URL used as the campaign source. |
| `content.message1` | body | `string` | yes | First message. |
| `content.message2` | body | `string` | no | Optional second follow-up message. |
| `content.message3` | body | `string` | no | Optional third follow-up message. |
