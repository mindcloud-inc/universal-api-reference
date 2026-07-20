# Sleekplan: Delete Post



```
DELETE https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/delete-post?connectionId=$CONNECTION_ID&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/delete-post?${params}`, {
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
| `postId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "feedbackId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `feedbackId` | number |  |

## Native endpoint

Through the native Sleekplan API, this operation is `DELETE /post/:postid` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

