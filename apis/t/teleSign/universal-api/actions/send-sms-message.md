# TeleSign: Send SMS Message



```
POST https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/send-sms-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/send-sms-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string",
  "message": "string",
  "messageType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/send-sms-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string",
    "message": "string",
    "messageType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes |  |
| `message` | string | yes |  |
| `messageType` | string | yes |  |
| `accountLifecycleEvent` | string | no |  |
| `originatingIp` | string | no |  |
| `externalId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reference_id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `POST /v1/messaging` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-message.md) for the provider-specific parameters and requirements.

