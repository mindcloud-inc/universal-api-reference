# Lettermint: Send Email

Sends a single email through Lettermint.

```
POST https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettermint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "subject": "string",
  "to[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "subject": "string",
    "to[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes |  |
| `subject` | string | yes |  |
| `to[]` | array<string> | yes |  |
| `html` | string | no |  |
| `text` | string | no |  |
| `tag` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string | Unique ID of the queued email message. |
| `status` | string | Current Lettermint delivery status for the message. |

## Native endpoint

Through the native Lettermint API, this operation is `POST /send` (base URL `https://api.lettermint.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

