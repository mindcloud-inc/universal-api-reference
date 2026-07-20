# Sendblue: Add Webhooks

Adds webhooks to Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/add-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/add-webhooks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhooks[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/add-webhooks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhooks[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhooks[]` | array<string> | yes | Webhook URLs to append. Accepts multiple values as an array. |
| `globalSecret` | string | no | Global secret for webhook signature verification. |
| `type` | string | no | The webhook event type to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string",
      "webhooks": {
        "receive": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |
| `webhooks.receive[]` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/account/webhooks` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhooks.md) for the provider-specific parameters and requirements.

