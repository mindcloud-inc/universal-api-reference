# Chatsistant: List Sessions

Retrieves chatbot session records from Chatsistant.

```
GET https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-sessions?${params}`, {
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
| `uuid` | string | no | The chatbot UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "ip_address": "string",
      "meta": {},
      "modified_at": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `ip_address` | string |  |
| `meta` | object |  |
| `modified_at` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Chatsistant API, this operation is `GET /chatbot/:uuid/sessions` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

