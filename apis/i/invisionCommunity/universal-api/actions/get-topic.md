# Invision Community: Get Topic



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-topic?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-topic?${params}`, {
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
| `id` | string | yes | The topic identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "posts": 1,
      "title": "string",
      "url": "https://example.com",
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Topic identifier. |
| `posts` | number | Post count in the topic. |
| `title` | string | Topic title. |
| `url` | string | Absolute URL to the topic. |
| `views` | number | View count for the topic. |

## Native endpoint

Through the native Invision Community API, this operation is `GET /forums/topics/:id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic.md) for the provider-specific parameters and requirements.

