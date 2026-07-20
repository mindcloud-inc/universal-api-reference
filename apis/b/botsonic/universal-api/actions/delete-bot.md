# Botsonic: Delete Bot

Deletes an existing bot from Botsonic.

```
DELETE https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-bot?connectionId=$CONNECTION_ID&botId=bot_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "bot_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-bot?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | bot_id of the bot to delete. Example: `bot_123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | no | Optional workspace identifier. Example: `workspace_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot_info_config": {},
      "bot_prompt_config": {},
      "bot_template_id": "string",
      "corresponding_cloned_bot_with_free_credits": "string",
      "created_at": "string",
      "deletion_datetime": "string",
      "id": "string",
      "is_cloned_for_free": true,
      "is_deleted": true,
      "is_sample_bot": true,
      "is_shared": true,
      "migration_status": "string",
      "owner_id": "string",
      "pinecone_index_config": "string",
      "updated_at": "string",
      "vectorstore": "string",
      "vectorstore_index_id": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot_info_config` | object | Bot information configuration. |
| `bot_prompt_config` | object | Bot prompt configuration. |
| `bot_template_id` | string | Bot template identifier. |
| `corresponding_cloned_bot_with_free_credits` | string | Free-credit cloned bot identifier. |
| `created_at` | string | Creation timestamp. |
| `deletion_datetime` | string | Deletion timestamp. |
| `id` | string | Bot identifier. |
| `is_cloned_for_free` | boolean | Whether the bot is cloned for free. |
| `is_deleted` | boolean | Whether the bot is deleted. |
| `is_sample_bot` | boolean | Whether the bot is a sample bot. |
| `is_shared` | boolean | Whether the bot is shared. |
| `migration_status` | string | Migration status. |
| `owner_id` | string | Owner identifier. |
| `pinecone_index_config` | string | Pinecone index configuration. |
| `updated_at` | string | Last update timestamp. |
| `vectorstore` | string | Vector store provider. |
| `vectorstore_index_id` | string | Vector store index identifier. |
| `workspace_id` | string | Workspace identifier. |

## Native endpoint

Through the native Botsonic API, this operation is `DELETE /v1/business/bot/:botId` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bot.md) for the provider-specific parameters and requirements.

