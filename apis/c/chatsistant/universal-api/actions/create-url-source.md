# Chatsistant: Create URL Source

Creates a new URL source in Chatsistant.

```
POST https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/create-url-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/create-url-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/create-url-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | The source URL. |
| `uuid` | string | no | The chatbot UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "file_name": "Ava Chen",
      "file_size": 1,
      "meta_json": "string",
      "modified_at": "string",
      "status": "string",
      "title": "string",
      "tokens": 1,
      "type": "string",
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
| `file_name` | string |  |
| `file_size` | number |  |
| `meta_json` | string |  |
| `modified_at` | string |  |
| `status` | string |  |
| `title` | string |  |
| `tokens` | number |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Chatsistant API, this operation is `POST /chatbot/:uuid/data-source/url` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-url-source.md) for the provider-specific parameters and requirements.

