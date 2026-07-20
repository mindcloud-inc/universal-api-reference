# Stormboard: List Storm Ideas

Retrieves ideas from a Storm in Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-ideas?connectionId=$CONNECTION_ID&stormId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stormId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-ideas?${params}`, {
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
| `lastModifiedMin` | string | no | Return ideas modified since this ISO 8601 timestamp. |
| `stormId` | number | yes | Storm ID from the Stormboard share dialog or related storm record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ideas": [
        {
          "color": "string",
          "comments": 1,
          "commentsUnread": 1,
          "created": {
            "date": "string"
          },
          "data": {
            "fontSize": 1,
            "name": "Ava Chen",
            "text": "string",
            "url": "https://example.com"
          },
          "id": 1,
          "legend": {
            "color": "string",
            "name": "Ava Chen"
          },
          "lock": 1,
          "modified": {
            "date": "string"
          },
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
          "votes": 1,
          "x": 1,
          "y": 1,
          "z": 1
        }
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ideas` | array<object> |  |
| `ideas[].color` | string |  |
| `ideas[].comments` | number |  |
| `ideas[].commentsUnread` | number |  |
| `ideas[].created` | object |  |
| `ideas[].created.date` | string |  |
| `ideas[].data` | object |  |
| `ideas[].data.fontSize` | number |  |
| `ideas[].data.name` | string |  |
| `ideas[].data.text` | string |  |
| `ideas[].data.url` | string |  |
| `ideas[].id` | number |  |
| `ideas[].legend` | object |  |
| `ideas[].legend.color` | string |  |
| `ideas[].legend.name` | string |  |
| `ideas[].lock` | number |  |
| `ideas[].modified` | object |  |
| `ideas[].modified.date` | string |  |
| `ideas[].myvotes` | number |  |
| `ideas[].shape` | string |  |
| `ideas[].storm` | object |  |
| `ideas[].storm.id` | number |  |
| `ideas[].storm.title` | string |  |
| `ideas[].task` | object |  |
| `ideas[].task.status` | string |  |
| `ideas[].type` | string |  |
| `ideas[].uuid` | string |  |
| `ideas[].votes` | number |  |
| `ideas[].x` | number |  |
| `ideas[].y` | number |  |
| `ideas[].z` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /storms/:storm_id/ideas` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storm-ideas.md) for the provider-specific parameters and requirements.

