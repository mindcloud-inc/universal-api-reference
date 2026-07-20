# CardClan: Send Card

Sends a personalized CardClan card by email.

```
POST https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/send-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/send-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "card": "string",
  "integrationId": "string",
  "mergeTags[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/send-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "card": "string",
    "integrationId": "string",
    "mergeTags[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `card` | string | yes | Card ID to send. |
| `emailAccount` | string | no | Email account ID or CardClan for the default sender. Default: `CardClan`. |
| `integrationId` | string | yes | Integration configuration ID. |
| `mergeTags[]` | array<object> | yes | Array of merge tag objects with recipient data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "recipient_id": "string",
      "status": true,
      "tracking_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider send result message. |
| `recipient_id` | string | CardClan recipient identifier. |
| `status` | boolean | Whether CardClan reported the send as successful. |
| `tracking_url` | string | Card tracking URL. |

## Native endpoint

Through the native CardClan API, this operation is `POST /integration/send-card` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-card.md) for the provider-specific parameters and requirements.

