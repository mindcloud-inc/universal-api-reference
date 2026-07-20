# Stackoverflow: List User Comments

Retrieves comments for specific users from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&ids=string&site=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-user-comments?${params}`, {
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
| `ids` | string | yes | Semicolon-delimited user IDs whose comments to list. |
| `site` | string | yes | API site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment_id": 1,
      "content_license": "string",
      "creation_date": "2026-05-07T12:00:00.000Z",
      "edited": true,
      "post_id": 1,
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment_id` | number |  |
| `content_license` | string |  |
| `creation_date` | date |  |
| `edited` | boolean |  |
| `post_id` | number |  |
| `score` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /users/[:ids]/comments` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-comments.md) for the provider-specific parameters and requirements.

