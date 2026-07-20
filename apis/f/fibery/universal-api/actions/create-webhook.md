# Fibery: Create Webhook

Creates a new webhook in Fibery.

```
POST https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Destination URL that should receive Fibery webhook events. |
| `type` | string | yes | Fibery type/database name to subscribe to, such as Space/Database. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "runs": [
        {}
      ],
      "state": "string",
      "type": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `runs` | array<object> |  |
| `state` | string |  |
| `type` | string |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /webhooks/v2` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

