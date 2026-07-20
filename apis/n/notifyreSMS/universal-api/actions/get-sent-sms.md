# Notifyre SMS: Get Sent SMS

Retrieves a sent SMS message from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sent-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sent-sms?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sent-sms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | Sent message identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "friendlyID": "string",
      "id": "string",
      "recipients": [
        {}
      ],
      "status": "string",
      "totalCost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `friendlyID` | string | Human-friendly message reference. |
| `id` | string | SMS message identifier. |
| `recipients` | array<object> | Recipients for the SMS message. |
| `status` | string | Overall message status. |
| `totalCost` | number | Total cost for the SMS message. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /sms/send/:messageId` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sent-sms.md) for the provider-specific parameters and requirements.

