# WhatsBoost: Link WhatsApp Account

Links a WhatsApp account in WhatsBoost.

```
POST https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/link-whats-app-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/link-whats-app-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/link-whats-app-account', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sid` | number | no | Optional WhatsApp server ID. If not provided, the system will automatically select the best available server from your package. You can get available server IDs from /get/wa.servers |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /create/wa.link` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-whats-app-account.md) for the provider-specific parameters and requirements.

