# SeaX: Upsert Messenger Integration

Updates Messenger integration settings in SeaX.

```
PUT https://connect.mindcloud.co/v1/universal/seaX/latest/actions/upsert-messenger-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/upsert-messenger-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/upsert-messenger-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "page_id": "string",
      "page_name": "Ava Chen",
      "service_provider_account_id": "string",
      "status": "string",
      "updated_time": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `page_id` | string |  |
| `page_name` | string |  |
| `service_provider_account_id` | string |  |
| `status` | string |  |
| `updated_time` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `PUT /messenger` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-messenger-integration.md) for the provider-specific parameters and requirements.

