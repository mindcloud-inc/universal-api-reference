# Selzy: Get Message

Retrieves a message from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-message?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "active_version_id": 1,
          "body": "string",
          "created": "string",
          "id": 1,
          "images_behavior": "string",
          "lang_code": "string",
          "last_update": "string",
          "list_id": 1,
          "message_format": "string",
          "sender_email": "ava@example.com",
          "sender_name": "Ava Chen",
          "service_type": "string",
          "sub_user_login": "string",
          "subject": "string",
          "text_body": "string",
          "wrap_type": "string"
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
| `result[].active_version_id` | number |  |
| `result[].body` | string |  |
| `result[].created` | string |  |
| `result[].id` | number |  |
| `result[].images_behavior` | string |  |
| `result[].lang_code` | string |  |
| `result[].last_update` | string |  |
| `result[].list_id` | number |  |
| `result[].message_format` | string |  |
| `result[].sender_email` | string |  |
| `result[].sender_name` | string |  |
| `result[].service_type` | string |  |
| `result[].sub_user_login` | string |  |
| `result[].subject` | string |  |
| `result[].text_body` | string |  |
| `result[].wrap_type` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getMessage` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

