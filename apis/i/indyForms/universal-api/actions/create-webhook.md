# IndyForms: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IndyForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/create-webhook', {
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
| `name` | string | no |  |
| `description` | string | no |  |
| `endpointAddress` | string | no |  |
| `raisedFor[]` | array<string> | no |  |
| `isActive` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endpointAddress": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "raisedFor": [
        "string"
      ],
      "sharedSecret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `endpointAddress` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `raisedFor` | array<string> |  |
| `sharedSecret` | string |  |

## Native endpoint

Through the native IndyForms API, this operation is `POST /api/public/v2/webhooks` (base URL `https://api.indyforms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

