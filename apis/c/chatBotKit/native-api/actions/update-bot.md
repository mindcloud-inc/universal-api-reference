# Update Bot with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/{botId}/update`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Update Bot](https://chatbotkit.com/manuals/bots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The ID of the bot to update |
| `alias` | body | `string` | no | Alias for the bot |
| `name` | body | `string` | no | Name of the bot |
| `description` | body | `string` | no | Description of the bot |
| `meta` | body | `object` | no | Metadata for the bot |
| `model` | body | `string` | no | Model used by the bot |
| `backstory` | body | `string` | no | Backstory for the bot |
| `datasetId` | body | `string` | no | Dataset ID for the bot |
| `skillsetId` | body | `string` | no | Skillset ID for the bot |
| `privacy` | body | `boolean` | no | Whether the bot is private |
| `moderation` | body | `boolean` | no | Whether moderation is enabled |
| `blueprintId` | body | `string` | no | Blueprint ID for the bot |
| `visibility` | body | `list` | no | Visibility of the bot Accepted values: `private`, `protected`, `public`. |
