# DataMotion: Track Secure Message

Retrieves secure message tracking details from DataMotion.

```
GET https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/track-secure-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMotion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/track-secure-message?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMotion/latest/actions/track-secure-message?${params}`, {
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
| `transactionId` | string | yes | Transaction ID of the secure message to track. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Attachments": [
        {}
      ],
      "Cost": 1,
      "ExpirationDate": "2026-05-07T12:00:00.000Z",
      "MessageId": 1,
      "MessageSize": 1,
      "SecurityEnvelope": {},
      "Subject": "string",
      "Tracking": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Attachments` | array<object> | Attachment tracking metadata. |
| `Cost` | number | Total transaction cost. |
| `ExpirationDate` | date | Message expiration date/time. |
| `MessageId` | number | Message identifier. |
| `MessageSize` | number | Message size in bytes. |
| `SecurityEnvelope` | object | Message security envelope object. |
| `Subject` | string | Message subject. |
| `Tracking` | array<object> | Recipient tracking entries. |

## Native endpoint

Through the native DataMotion API, this operation is `GET /v1.2/:transactionId/Track` (base URL `https://api.datamotion.com/SecureMessageDelivery`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-secure-message.md) for the provider-specific parameters and requirements.

