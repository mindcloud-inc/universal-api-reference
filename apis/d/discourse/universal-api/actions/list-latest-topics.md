# Discourse: List Latest Topics

Retrieves the latest topics from Discourse.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-latest-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-latest-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-latest-topics?${params}`, {
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
| `ascending` | string | no | Set to true to sort ascending. |
| `order` | string | no | Sort order for latest topics, such as default, created, or activity. |

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
| `flair_groups` | array<object> | Flair groups referenced by the latest topics response. |
| `primary_groups` | array<object> | Primary groups referenced by the latest topics response. |
| `topic_list` | object | Container with pagination metadata and the list of latest topics. |
| `users` | array<object> | Users referenced in the latest topics response, including poster metadata. |

## Native endpoint

Through the native Discourse API, this operation is `GET /latest.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-latest-topics.md) for the provider-specific parameters and requirements.

