# Instasent: Get SMS



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-sms?connectionId=$CONNECTION_ID&project=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-sms?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `id` | string | yes | SMS identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity": {
        "allowUnicode": true,
        "audienceContact": {
          "id": "string",
          "project": "string"
        },
        "charged": true,
        "charsCount": 1,
        "country": "string",
        "deliveredAt": "string",
        "deliveredText": "string",
        "encoding": "string",
        "from": "string",
        "id": "string",
        "inbound": true,
        "messagesCount": 1,
        "metadata": {},
        "normalizedTo": "string",
        "pricePerSms": 1,
        "priceUser": 1,
        "scheduledAt": "string",
        "sentAt": "string",
        "status": "string",
        "statusCode": "string",
        "text": "string",
        "to": "string",
        "unicode": true
      },
      "metadata": {
        "audienceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.allowUnicode` | boolean | Whether Unicode sending was allowed |
| `entity.audienceContact.id` | string | Associated audience contact identifier |
| `entity.audienceContact.project` | string | Associated project identifier on the audience contact |
| `entity.charged` | boolean | Whether the message was billed |
| `entity.charsCount` | number | Character count for the message |
| `entity.country` | string | Recipient country code |
| `entity.deliveredAt` | string | Timestamp when the message was delivered |
| `entity.deliveredText` | string | Rendered text delivered to the recipient |
| `entity.encoding` | string | SMS encoding used for the message |
| `entity.from` | string | Sender id or phone number |
| `entity.id` | string | SMS message identifier |
| `entity.inbound` | boolean | Whether the message is inbound |
| `entity.messagesCount` | number | Number of SMS parts used by the message |
| `entity.metadata` | object | Additional SMS metadata payload |
| `entity.normalizedTo` | string | Normalized recipient phone number |
| `entity.pricePerSms` | number | Price per SMS segment |
| `entity.priceUser` | number | Total price charged to the user |
| `entity.scheduledAt` | string | Timestamp when the message is scheduled to be sent |
| `entity.sentAt` | string | Timestamp when the message was sent |
| `entity.status` | string | SMS delivery status |
| `entity.statusCode` | string | Provider status code when available |
| `entity.text` | string | Original SMS text |
| `entity.to` | string | Recipient phone number |
| `entity.unicode` | boolean | Whether the message contains Unicode characters |
| `metadata.audienceId` | string | Associated audience contact identifier |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/channel/sms/sms/:id` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms.md) for the provider-specific parameters and requirements.

