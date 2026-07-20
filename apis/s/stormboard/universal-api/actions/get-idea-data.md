# Stormboard: Get Idea Data

Retrieves idea data from Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-idea-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-idea-data?connectionId=$CONNECTION_ID&ideaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ideaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-idea-data?${params}`, {
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
| `ideaId` | number | yes | Idea ID from a Stormboard idea record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "idea": {
        "color": "string",
        "comments": 1,
        "commentsUnread": 1,
        "data": {
          "fontSize": 1,
          "name": "Ava Chen",
          "text": "string",
          "url": "https://example.com"
        },
        "id": 1,
        "myvotes": 1,
        "shape": "string",
        "storm": {
          "id": 1,
          "title": "string"
        },
        "task": {
          "status": "string"
        },
        "type": "string",
        "uuid": "string",
        "votes": 1
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `idea` | object |  |
| `idea.color` | string |  |
| `idea.comments` | number |  |
| `idea.commentsUnread` | number |  |
| `idea.data` | object |  |
| `idea.data.fontSize` | number |  |
| `idea.data.name` | string |  |
| `idea.data.text` | string |  |
| `idea.data.url` | string |  |
| `idea.id` | number |  |
| `idea.myvotes` | number |  |
| `idea.shape` | string |  |
| `idea.storm` | object |  |
| `idea.storm.id` | number |  |
| `idea.storm.title` | string |  |
| `idea.task` | object |  |
| `idea.task.status` | string |  |
| `idea.type` | string |  |
| `idea.uuid` | string |  |
| `idea.votes` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /ideas/:idea_id` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-idea-data.md) for the provider-specific parameters and requirements.

