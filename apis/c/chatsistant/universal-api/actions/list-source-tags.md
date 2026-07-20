# Chatsistant: List Source Tags

Retrieves source tag records from Chatsistant.

```
GET https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-source-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-source-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-source-tags?${params}`, {
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

Through the native Chatsistant API, this operation is `GET /chatbot/:uuid/source-tags` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-source-tags.md) for the provider-specific parameters and requirements.

