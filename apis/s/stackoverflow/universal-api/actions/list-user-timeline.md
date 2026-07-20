# Stackoverflow: List User Timeline

Retrieves timeline entries for specific users from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-timeline?connectionId=$CONNECTION_ID&limit=25&offset=0&ids=string&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ids": "string",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-timeline?${params}`, {
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
| `ids` | string | yes | Semicolon-delimited user IDs whose timeline to list. |
| `site` | string | yes | API site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badge_id": 1,
      "comment_id": 1,
      "creation_date": "2026-05-07T12:00:00.000Z",
      "post_id": 1,
      "suggested_edit_id": 1,
      "timeline_type": "string",
      "title": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badge_id` | number |  |
| `comment_id` | number |  |
| `creation_date` | date |  |
| `post_id` | number |  |
| `suggested_edit_id` | number |  |
| `timeline_type` | string |  |
| `title` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /users/[:ids]/timeline` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-timeline.md) for the provider-specific parameters and requirements.

