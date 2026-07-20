# Superthread: List Comments for a Resource



```
GET https://connect.mindcloud.co/v1/universal/superthread/latest/actions/list-comments-for-a-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/list-comments-for-a-resource?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superthread/latest/actions/list-comments-for-a-resource?${params}`, {
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
| `teamId` | string | yes |  |
| `pageId` | string | no |  |
| `cardId` | string | no |  |
| `filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "count": 1,
      "cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `count` | number |  |
| `cursor` | string |  |

## Native endpoint

Through the native Superthread API, this operation is `GET /:team_id/comments` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments-for-a-resource.md) for the provider-specific parameters and requirements.

