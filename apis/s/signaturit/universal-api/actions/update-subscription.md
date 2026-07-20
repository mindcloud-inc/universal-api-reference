# Signaturit: Update Subscription

Updates an existing subscription in Signaturit.

```
PUT https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "d4c2a480-22f1-11f1-b406-066f594717e9",
  "url": "https://httpbin.org/post.json?updated=1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/update-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "d4c2a480-22f1-11f1-b406-066f594717e9",
    "url": "https://httpbin.org/post.json?updated=1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Identifier of the subscription to update. Example: `d4c2a480-22f1-11f1-b406-066f594717e9`. |
| `url` | string | yes | Destination URL that will receive Signaturit event payloads. Example: `https://httpbin.org/post.json?updated=1`. |
| `events` | string | no | Optional replacement event code or * wildcard. The docs say update accepts the same parameters as create. Example: `*`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
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
| `createdAt` | string |  |
| `events[]` | string |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `PATCH /subscriptions/:id.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

