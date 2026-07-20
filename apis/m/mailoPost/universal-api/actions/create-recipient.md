# MailoPost: Create Recipient

Creates a new recipient in a MailoPost list.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MailoPost recipient list identifier. |
| `email` | string | yes | Recipient email address. |
| `values[]` | array<object> | no | Recipient parameter values. |
| `tags[]` | array<string> | no | Recipient tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unconfirmed` | boolean | no | Create recipient as unconfirmed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmed": true,
      "email": "ava@example.com",
      "id": 1,
      "list_id": 1,
      "status": "string",
      "tags": [
        "string"
      ],
      "values": [
        {
          "kind": "string",
          "parameter_id": 1,
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `list_id` | number |  |
| `status` | string |  |
| `tags[]` | string |  |
| `values[].kind` | string |  |
| `values[].parameter_id` | number |  |
| `values[].value` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `POST /email/lists/:id/recipients` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient.md) for the provider-specific parameters and requirements.

