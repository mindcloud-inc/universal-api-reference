# Handwrite: Send Letter

Sends a handwritten letter through Handwrite.

```
POST https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/send-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/send-letter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "handwriting": "string",
  "card": "string",
  "recipients[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/send-letter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "handwriting": "string",
    "card": "string",
    "recipients[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | Letter body text. Handwrite documents a maximum of 320 characters. |
| `handwriting` | string | yes | The handwriting ID to use for the letter. |
| `card` | string | yes | The stationery or card ID to use for the letter. |
| `recipients[]` | array<object> | yes | Array of recipient objects. Each recipient should include address fields such as firstName, lastName, street1, city, state, and zip. |
| `from` | object | no | Optional return-address object with firstName, lastName, street1, street2, city, state, and zip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "card": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "environment": "string",
      "from": {},
      "handwriting": "string",
      "message": "string",
      "meta": {},
      "origin": "string",
      "proofs": [
        {}
      ],
      "status": "string",
      "to": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Created Handwrite order ID. |
| `card` | string | Selected stationery ID. |
| `createdAt` | date | Order creation timestamp. |
| `environment` | string | Handwrite environment for the order. |
| `from` | object | Sender object returned by Handwrite when provided. |
| `handwriting` | string | Selected handwriting ID. |
| `message` | string | Letter message text. |
| `meta` | object | Additional metadata returned by Handwrite. |
| `origin` | string | Order creation origin. |
| `proofs` | array<object> | Proof image records for completed orders. |
| `status` | string | Order status such as processing, written, complete, problem, or cancelled. |
| `to` | object | Recipient object returned by Handwrite. |

## Native endpoint

Through the native Handwrite API, this operation is `POST /send` (base URL `https://api.handwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-letter.md) for the provider-specific parameters and requirements.

