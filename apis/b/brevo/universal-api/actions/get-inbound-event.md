# Brevo: Get Inbound Event



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-inbound-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-inbound-event?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-inbound-event?${params}`, {
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
| `uuid` | string | yes | The inbound event UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "logs": [
        {}
      ],
      "messageId": "string",
      "receivedAt": "string",
      "recipient": "string",
      "sender": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | The inbound attachments. |
| `logs` | array<object> | The event log history. |
| `messageId` | string | The inbound message id. |
| `receivedAt` | string | The received timestamp. |
| `recipient` | string | The inbound recipient. |
| `sender` | string | The inbound sender. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/inbound/events/:uuid` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbound-event.md) for the provider-specific parameters and requirements.

