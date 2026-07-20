# Court Drive: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpointUrl": "https://example.com",
  "subscribedEvents[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpointUrl": "https://example.com",
    "subscribedEvents[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpointUrl` | string | yes | Webhook endpoint URL to receive CourtAPI events. |
| `subscribedEvents[]` | array<string> | yes | List of CourtAPI event names to subscribe the webhook to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {},
      "webhook": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | object |  |
| `webhook` | object |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /webhooks` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

