# Chatsistant: Update Source Tag

Updates an existing source tag in Chatsistant.

```
PUT https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-source-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-source-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-source-tag', {
  method: 'PUT',
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
| `color` | string | no | The source tag color. |
| `name` | string | no | The source tag name. |
| `uuid` | string | no | The tag UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "string",
      "data_source_uuids": [
        "string"
      ],
      "modified_at": "string",
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | string |  |
| `data_source_uuids` | array<string> |  |
| `modified_at` | string |  |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Chatsistant API, this operation is `POST /source-tag/:uuid/update` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source-tag.md) for the provider-specific parameters and requirements.

