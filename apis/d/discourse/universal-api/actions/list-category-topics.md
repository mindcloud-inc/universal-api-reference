# Discourse: List Category Topics

Retrieves topics from a Discourse category.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-category-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-category-topics?connectionId=$CONNECTION_ID&id=string&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-category-topics?${params}`, {
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
| `id` | string | yes | Numeric Discourse category ID. |
| `slug` | string | yes | Category slug used in the category URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flair_groups": [
        {}
      ],
      "primary_groups": [
        {}
      ],
      "topic_list": {},
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flair_groups` | array<object> |  |
| `primary_groups` | array<object> |  |
| `topic_list` | object |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /c/:slug/:id.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-category-topics.md) for the provider-specific parameters and requirements.

