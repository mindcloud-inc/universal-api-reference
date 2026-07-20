# Create Bot with Botsonic

Creates a new bot in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Create Bot](https://docs.botsonic.com/reference/create_bot_v1_business_bot_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `string` | no | Optional workspace identifier. |
| `id` | body | `string` | no | Optional bot identifier. |
| `bot_name` | body | `string` | no | Bot name. |
| `workspace_id` | body | `string` | no | Optional workspace_id in the create bot request body. |
| `utm_params` | body | `string` | no | Optional UTM parameters. |
| `bot_template_id` | body | `string` | no | Bot template identifier. |
| `model` | body | `string` | no | AI model for the bot. |
| `is_shared` | body | `boolean` | no | Whether the bot is shared. |
| `bot_avatar_icon` | body | `string` | no | Optional bot avatar icon. |
| `company_logo` | body | `string` | no | Optional company logo. |
| `is_sample_bot` | body | `boolean` | no | Whether the bot is a sample bot. |
| `vector_prefix` | body | `string` | no | Optional vector prefix. |
