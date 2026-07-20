# Eversign: Send Reminder

Sends a signer reminder in Eversign.

```
PUT https://connect.mindcloud.co/v1/universal/eversign/latest/actions/send-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/send-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentHash": "string",
  "signerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eversign/latest/actions/send-reminder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentHash": "string",
    "signerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentHash` | string | yes |  |
| `signerId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Eversign API, this operation is `POST /send_reminder` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reminder.md) for the provider-specific parameters and requirements.

