# MailoPost: Update Recipient

Updates an existing recipient in a MailoPost list.

```
PUT https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "id": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-recipient', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
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
| `listId` | string | yes | MailoPost recipient list identifier. |
| `id` | string | yes | MailoPost recipient identifier. |
| `email` | string | yes | Recipient email address. |
| `values[]` | array<object> | no | Recipient parameter values. |
| `tags[]` | array<string> | no | Recipient tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runTriggers` | boolean | no | Run recipient triggers after the update. |

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

Through the native MailoPost API, this operation is `PATCH /email/lists/:list_id/recipients/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient.md) for the provider-specific parameters and requirements.

