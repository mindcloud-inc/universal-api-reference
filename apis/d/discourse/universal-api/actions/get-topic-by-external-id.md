# Discourse: Get Topic By External ID

Retrieves a Discourse topic by external ID.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic-by-external-id?connectionId=$CONNECTION_ID&external_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "external_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic-by-external-id?${params}`, {
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
| `external_id` | string | yes | External topic identifier configured in Discourse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category_id": 1,
      "details": {},
      "fancy_title": "string",
      "id": 1,
      "post_stream": {},
      "posts_count": 1,
      "slug": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category_id` | number |  |
| `details` | object |  |
| `fancy_title` | string |  |
| `id` | number |  |
| `post_stream` | object |  |
| `posts_count` | number |  |
| `slug` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /t/external_id/:external_id.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic-by-external-id.md) for the provider-specific parameters and requirements.

