# ChatBotKit: List Files



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-files?${params}`, {
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
| `cursor` | string | no | The cursor to use for pagination |
| `order` | list | no | The order of the paginated items One of: `asc`, `desc`. |
| `take` | number | no | The number of items to retrieve |
| `meta` | object | no | Key-value pairs to filter the partner users by metadata |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {
          "blueprintId": "string",
          "createdAt": 1,
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "updatedAt": 1,
          "visibility": "string"
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
| `cursor` | string |  |
| `items[].blueprintId` | string |  |
| `items[].createdAt` | number |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].updatedAt` | number |  |
| `items[].visibility` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /file/list` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

