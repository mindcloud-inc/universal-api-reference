# Botsonic: Delete Bot Data

Deletes existing bot data from Botsonic.

```
DELETE https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-bot-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-bot-data?connectionId=$CONNECTION_ID&dataId=data_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataId": "data_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-bot-data?${params}`, {
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
| `dataId` | string | yes | data_id of the bot data item. Example: `data_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot_id": "string",
      "characters": 1,
      "container_id": "string",
      "created_at": "string",
      "error_reason": "string",
      "file_type": "string",
      "id": "string",
      "integration_id": "string",
      "is_deleted": true,
      "is_paused": true,
      "is_private": true,
      "last_trained_at": "string",
      "migration_status": "string",
      "num_timed_out": 1,
      "resync_job_id": "string",
      "sitemap_id": "string",
      "status": "string",
      "storage_account_id": "string",
      "third_party_id": "string",
      "title": "string",
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot_id` | string | Bot identifier. |
| `characters` | number | Character count. |
| `container_id` | string | Container identifier. |
| `created_at` | string | Creation timestamp. |
| `error_reason` | string | Processing error reason. |
| `file_type` | string | File type. |
| `id` | string | Bot data identifier. |
| `integration_id` | string | Integration identifier. |
| `is_deleted` | boolean | Whether the data item is deleted. |
| `is_paused` | boolean | Whether source sync is paused. |
| `is_private` | boolean | Whether the source is private. |
| `last_trained_at` | string | Last trained timestamp. |
| `migration_status` | string | Migration status. |
| `num_timed_out` | number | Timed-out record count. |
| `resync_job_id` | string | Resync job identifier. |
| `sitemap_id` | string | Sitemap identifier. |
| `status` | string | Processing status. |
| `storage_account_id` | string | Storage account identifier. |
| `third_party_id` | string | Third-party source identifier. |
| `title` | string | Source title. |
| `updated_at` | string | Last update timestamp. |
| `url` | string | Source URL. |

## Native endpoint

Through the native Botsonic API, this operation is `DELETE /v1/business/bot-data/:dataId` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bot-data.md) for the provider-specific parameters and requirements.

