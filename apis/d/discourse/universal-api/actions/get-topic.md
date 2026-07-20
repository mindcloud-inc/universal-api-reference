# Discourse: Get Topic

Retrieves a single topic from Discourse.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-topic?${params}`, {
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
| `id` | string | yes | Numeric Discourse topic ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "fancy_title": "string",
      "id": 1,
      "post_stream": {},
      "slug": "string",
      "suggested_topics": [
        {}
      ],
      "tags": [
        "string"
      ],
      "timeline_lookup": [
        [
          "string"
        ]
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object |  |
| `fancy_title` | string |  |
| `id` | number |  |
| `post_stream` | object |  |
| `slug` | string |  |
| `suggested_topics` | array<object> |  |
| `tags` | array<string> |  |
| `timeline_lookup` | array<array> |  |
| `title` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /t/:id.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic.md) for the provider-specific parameters and requirements.

