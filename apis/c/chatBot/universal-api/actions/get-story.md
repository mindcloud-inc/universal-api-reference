# ChatBot: Get Story

Retrieves chatbot story details from ChatBot API.

```
GET https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-story?connectionId=$CONNECTION_ID&storyId=69bae96bb878760007d62dfb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyId": "69bae96bb878760007d62dfb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/get-story?${params}`, {
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
| `storyId` | string | yes | The required ChatBot story ID from the request path. Example: `69bae96bb878760007d62dfb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "diagram": {},
      "history": {},
      "id": "string",
      "name": "Ava Chen",
      "published": true,
      "settings": {},
      "state": {},
      "userSettings": {},
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `diagram` | object |  |
| `history` | object |  |
| `id` | string |  |
| `name` | string |  |
| `published` | boolean |  |
| `settings` | object |  |
| `state` | object |  |
| `userSettings` | object |  |
| `version` | number |  |

## Native endpoint

Through the native ChatBot API, this operation is `GET /v2/stories/:storyId` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story.md) for the provider-specific parameters and requirements.

