# ChatBotKit: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-conversations?${params}`, {
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
          "backstory": "string",
          "botId": "string",
          "contactId": "string",
          "createdAt": 1,
          "datasetId": "string",
          "description": "string",
          "id": "string",
          "model": "string",
          "moderation": true,
          "name": "Ava Chen",
          "privacy": true,
          "skillsetId": "string",
          "spaceId": "string",
          "taskId": "string",
          "updatedAt": 1
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
| `items[].botId` | string |  |
| `items[].contactId` | string |  |
| `items[].createdAt` | number |  |
| `items[].datasetId` | string |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].model` | string |  |
| `items[].moderation` | boolean |  |
| `items[].name` | string |  |
| `items[].privacy` | boolean |  |
| `items[].skillsetId` | string |  |
| `items[].spaceId` | string |  |
| `items[].taskId` | string |  |
| `items[].updatedAt` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /conversation/list` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

