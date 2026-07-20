# Dropmark: Get Activity Feed



```
GET https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity-feed?connectionId=$CONNECTION_ID&format=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "format": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropmark/latest/actions/get-activity-feed?${params}`, {
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
| `format` | string | yes | Raw activity feed representation. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "format": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Raw activity feed response body. |
| `format` | string | Requested feed format. |

## Native endpoint

Through the native Dropmark API, this operation is `GET /activity.{{args.format}}` (base URL `https://{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-feed.md) for the provider-specific parameters and requirements.

