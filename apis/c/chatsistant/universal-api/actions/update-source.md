# Chatsistant: Update Source

Updates an existing source in Chatsistant.

```
PUT https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Updated title for the data source. |
| `uuid` | string | yes | The source UUID. |

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

Through the native Chatsistant API, this operation is `POST /data-source/:uuid/update` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source.md) for the provider-specific parameters and requirements.

