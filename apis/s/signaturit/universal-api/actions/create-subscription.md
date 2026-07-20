# Signaturit: Create Subscription

Creates a new subscription in Signaturit.

```
POST https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://httpbin.org/post.json",
  "events": "*"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://httpbin.org/post.json",
    "events": "*"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Destination URL that will receive Signaturit event payloads. Example: `https://httpbin.org/post.json`. |
| `events` | string | yes | Signaturit event code to subscribe to. Example: `*`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "events": [
        "string"
      ],
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `events[]` | string |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `POST /subscriptions.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

