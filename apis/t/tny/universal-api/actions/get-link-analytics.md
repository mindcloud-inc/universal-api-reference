# Tny: Get Link Analytics

Retrieves analytics for a short link from Tny.

```
GET https://connect.mindcloud.co/v1/universal/tny/latest/actions/get-link-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tny/latest/actions/get-link-analytics?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tny/latest/actions/get-link-analytics?${params}`, {
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
| `slug` | string | yes | The short link slug to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytics": {},
      "link": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytics` | object | Analytics breakdown for the requested short URL. |
| `link` | object | Link metadata for the requested short URL. |

## Native endpoint

Through the native Tny API, this operation is `GET /api/v1/analytics/:slug` (base URL `https://www.tny.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-analytics.md) for the provider-specific parameters and requirements.

