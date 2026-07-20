# Documenso: Get Recipient

Retrieves a recipient from Documenso.

```
GET https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-recipient?connectionId=$CONNECTION_ID&recipientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-recipient?${params}`, {
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
| `recipientId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "envelopeId": "string",
      "fields": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "readStatus": "string",
      "role": "string",
      "sendStatus": "string",
      "signingOrder": 1,
      "signingStatus": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `envelopeId` | string |  |
| `fields` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `readStatus` | string |  |
| `role` | string |  |
| `sendStatus` | string |  |
| `signingOrder` | number |  |
| `signingStatus` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Documenso API, this operation is `GET /envelope/recipient/:recipientId` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient.md) for the provider-specific parameters and requirements.

