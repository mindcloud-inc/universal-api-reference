# CastingWords: Order Captions And Timestamps

Creates a transcript order with captions and timestamps in CastingWords.

```
POST https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/order-captions-and-timestamps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CastingWords `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/order-captions-and-timestamps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/order-captions-and-timestamps', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public audio or video URL to transcribe. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `test` | string | no | Set to 1 to run a CastingWords test order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audiofiles": [
        1
      ],
      "message": "string",
      "order": "string",
      "test_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audiofiles` | array<number> | Created or simulated audiofile IDs. |
| `message` | string | CastingWords order result message. |
| `order` | string | CastingWords order identifier. |
| `test_message` | string | Provider test-mode note when present. |

## Native endpoint

Through the native CastingWords API, this operation is `POST order_url` (base URL `https://castingwords.com/store/API4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/order-captions-and-timestamps.md) for the provider-specific parameters and requirements.

