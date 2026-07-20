# Sendblue: Send Read Receipt

Sends a read receipt through Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-read-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-read-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string",
  "fromNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-read-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string",
    "fromNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | The conversation phone number to mark as read in E.164 format. |
| `fromNumber` | string | yes | Your Sendblue line number in E.164 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "number": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `number` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/mark-read` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-read-receipt.md) for the provider-specific parameters and requirements.

