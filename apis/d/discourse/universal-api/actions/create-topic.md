# Discourse: Create Topic

Creates a new topic in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "raw": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-topic', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "raw": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Topic title. Required when creating a new topic. |
| `raw` | string | yes | Topic body in raw Discourse markdown. |
| `category` | number | no | Optional category id for the new topic. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `external_id` | string | no | Optional external system id to associate with the new topic. |
| `auto_track` | boolean | no | Set false to avoid automatically tracking the new topic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "post_number": 1,
      "post_url": "https://example.com",
      "raw": "string",
      "topic_id": 1,
      "topic_slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `post_number` | number |  |
| `post_url` | string |  |
| `raw` | string |  |
| `topic_id` | number |  |
| `topic_slug` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /posts.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-topic.md) for the provider-specific parameters and requirements.

