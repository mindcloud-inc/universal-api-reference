# Invidious: Resolve URL



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/resolve-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/resolve-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DdQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/resolve-url?${params}`, {
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
| `url` | string | yes | YouTube or Invidious URL to resolve. Example: `https://www.youtube.com/watch?v=dQw4w9WgXcQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string",
      "ucid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |
| `ucid` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /resolveurl` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-url.md) for the provider-specific parameters and requirements.

