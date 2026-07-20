# ChatBotKit: List Bots



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-bots?${params}`, {
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
| `cursor` | string | no | Cursor for fetching the next page. |
| `order` | list | no | Order of the paginated items. One of: `asc`, `desc`. |
| `take` | number | no | Number of items to retrieve. |
| `meta` | object | no | Filter bots by metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {
          "backstory": "string",
          "blueprintId": "string",
          "createdAt": 1,
          "datasetId": "string",
          "description": "string",
          "id": "string",
          "model": "string",
          "moderation": true,
          "name": "Ava Chen",
          "privacy": true,
          "skillsetId": "string",
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
| `items[].backstory` | string |  |
| `items[].blueprintId` | string |  |
| `items[].createdAt` | number |  |
| `items[].datasetId` | string |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].model` | string |  |
| `items[].moderation` | boolean |  |
| `items[].name` | string |  |
| `items[].privacy` | boolean |  |
| `items[].skillsetId` | string |  |
| `items[].updatedAt` | number |  |
| `items[].visibility` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /bot/list` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bots.md) for the provider-specific parameters and requirements.

