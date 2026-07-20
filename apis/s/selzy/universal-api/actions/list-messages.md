# Selzy: List Messages

Retrieves messages from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-messages?connectionId=$CONNECTION_ID&dateFrom=string&dateTo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "string",
  "dateTo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-messages?${params}`, {
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
| `dateFrom` | string | yes | Lower UTC bound for message creation time in YYYY-MM-DD hh:mm format. |
| `dateTo` | string | yes | Upper UTC bound for message creation time in YYYY-MM-DD hh:mm format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of messages to return, from 1 to 100. |
| `offset` | number | no | Zero-based starting position for the result set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "created": "string",
          "id": 1,
          "lang_code": "string",
          "list_id": 1,
          "login": "string",
          "message_format": "string",
          "segment_id": 1,
          "sender_email": "ava@example.com",
          "sender_name": "Ava Chen",
          "service_type": "string",
          "sub_user_login": "string",
          "subject": "string",
          "updated": "string"
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
| `result[].created` | string |  |
| `result[].id` | number |  |
| `result[].lang_code` | string |  |
| `result[].list_id` | number |  |
| `result[].login` | string |  |
| `result[].message_format` | string |  |
| `result[].segment_id` | number |  |
| `result[].sender_email` | string |  |
| `result[].sender_name` | string |  |
| `result[].service_type` | string |  |
| `result[].sub_user_login` | string |  |
| `result[].subject` | string |  |
| `result[].updated` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getMessages` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

