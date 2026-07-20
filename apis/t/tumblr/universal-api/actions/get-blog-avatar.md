# Tumblr: Get Blog Avatar

Retrieves a Tumblr blog avatar by size.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-blog-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-blog-avatar?connectionId=$CONNECTION_ID&blogIdentifier=string&size=64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string",
  "size": "64"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-blog-avatar?${params}`, {
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
| `blogIdentifier` | string | yes | Any blog identifier. |
| `size` | list<number> | yes | Avatar size in pixels. One of: `128`, `16`, `24`, `30`, `40`, `48`, `512`, `64`, `96`. Default: `64`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/avatar/:size` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blog-avatar.md) for the provider-specific parameters and requirements.

