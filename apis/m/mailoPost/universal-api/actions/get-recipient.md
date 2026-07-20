# MailoPost: Get Recipient

Retrieves a recipient from a MailoPost list.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-recipient?connectionId=$CONNECTION_ID&listId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-recipient?${params}`, {
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
| `listId` | string | yes | MailoPost recipient list identifier. |
| `id` | string | yes | MailoPost recipient identifier. |

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

Through the native MailoPost API, this operation is `GET /email/lists/:list_id/recipients/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient.md) for the provider-specific parameters and requirements.

