# Heyy: List Message Templates

Retrieves message templates from a Heyy workspace.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-message-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-message-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-message-templates?${params}`, {
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
      "category": "string",
      "components": [
        {}
      ],
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `components` | array<object> |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Heyy API, this operation is `GET /message_templates` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-templates.md) for the provider-specific parameters and requirements.

