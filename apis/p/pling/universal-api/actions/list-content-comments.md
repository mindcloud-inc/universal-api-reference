# Pling: List Content Comments

Retrieves public content comments from Pling.

```
GET https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pling `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&type=string&contentId=string&contentId2=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "type": "string",
  "contentId": "string",
  "contentId2": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content-comments?${params}`, {
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
| `type` | string | yes | OCS comment type. Use 1 for content comments. |
| `contentId` | string | yes | Pling content identifier whose comments should be listed. |
| `contentId2` | string | yes | Second OCS identifier segment; use 0 for top-level content comments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": [
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
| `comment` | array<object> | Content comments returned by Pling. |

## Native endpoint

Through the native Pling API, this operation is `GET /comments/data/:type/:contentId/:contentId2` (base URL `https://api.pling.com/ocs/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-content-comments.md) for the provider-specific parameters and requirements.

