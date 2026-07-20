# Pinboard: Delete Bookmark



```
DELETE https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/delete-bookmark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/delete-bookmark?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/delete-bookmark?${params}`, {
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
| `url` | string | yes | Bookmark URL to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result_code` | string | Pinboard result code. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /posts/delete` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bookmark.md) for the provider-specific parameters and requirements.

