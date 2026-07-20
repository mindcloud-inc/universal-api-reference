# SeaX: Sync WhatsApp Business Platform By Code

Adds a WhatsApp Business Platform account to SeaX by code.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/sync-whatsapp-business-platform-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/sync-whatsapp-business-platform-by-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/sync-whatsapp-business-platform-by-code', {
  method: 'POST',
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
      "id": "string",
      "is_deleted": true,
      "phones": [
        {}
      ],
      "service_account_id": "string",
      "service_account_name": "Ava Chen",
      "service_name": "Ava Chen",
      "status": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `is_deleted` | boolean |  |
| `phones` | array<object> |  |
| `service_account_id` | string |  |
| `service_account_name` | string |  |
| `service_name` | string |  |
| `status` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /whatsapp_business_platform` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-whatsapp-business-platform-by-code.md) for the provider-specific parameters and requirements.

