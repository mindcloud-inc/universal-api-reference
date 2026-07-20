# Seven: Validate Sender for Voice

Creates a voice sender validation in Seven.

```
POST https://connect.mindcloud.co/v1/universal/seven/latest/actions/validate-sender-for-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seven/latest/actions/validate-sender-for-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seven/latest/actions/validate-sender-for-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | The phone number to be validated. The format is almost arbitrary - our gateway automatically formats the number correctly. |
| `callback` | string | no | Callback URL to be called as soon as the validation has been successfully completed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "error": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `error` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `POST /validate_for_voice` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-sender-for-voice.md) for the provider-specific parameters and requirements.

