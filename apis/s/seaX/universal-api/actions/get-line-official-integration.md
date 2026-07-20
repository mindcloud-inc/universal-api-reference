# SeaX: Get LINE Official Integration

Retrieves LINE Official integration settings from SeaX by phone.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-line-official-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-line-official-integration?connectionId=$CONNECTION_ID&phoneId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-line-official-integration?${params}`, {
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
| `phoneId` | string | yes | Phone identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot_basic_id": "string",
      "channel_id": "string",
      "created_time": "string",
      "rich_menu_id": "string",
      "service_provider_account_id": "string",
      "status": "string",
      "updated_time": "string",
      "webhook_enabled": true,
      "webhook_endpoint": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot_basic_id` | string |  |
| `channel_id` | string |  |
| `created_time` | string |  |
| `rich_menu_id` | string |  |
| `service_provider_account_id` | string |  |
| `status` | string |  |
| `updated_time` | string |  |
| `webhook_enabled` | boolean |  |
| `webhook_endpoint` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `GET /line_official/phone/{phone_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-line-official-integration.md) for the provider-specific parameters and requirements.

