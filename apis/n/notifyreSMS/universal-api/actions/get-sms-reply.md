# Notifyre SMS: Get SMS Reply

Retrieves an SMS reply from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sms-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sms-reply?connectionId=$CONNECTION_ID&replyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "replyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/get-sms-reply?${params}`, {
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
| `replyId` | string | yes | Reply identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "receivedDateUtc": 1,
      "recipientID": "string",
      "replyID": "string",
      "senderNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Reply message body. |
| `receivedDateUtc` | number | UTC timestamp when the reply was received. |
| `recipientID` | string | Recipient identifier associated with the reply. |
| `replyID` | string | Reply identifier. |
| `senderNumber` | string | Originating sender number. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /sms/received/:replyId` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-reply.md) for the provider-specific parameters and requirements.

