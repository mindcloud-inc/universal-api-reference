# Shibe.online: Get Random Cat Images



```
GET https://connect.mindcloud.co/v1/universal/shibeonline/latest/actions/get-random-cat-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shibe.online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shibeonline/latest/actions/get-random-cat-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shibeonline/latest/actions/get-random-cat-images?${params}`, {
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
| `count` | number | no | Number of images to return (1 through 100). Default: `1`. |
| `urls` | boolean | no | When true, return image URLs; when false, the provider can return non-URL values. Default: `true`. |
| `httpsUrls` | boolean | no | When returning URLs, request HTTPS image URLs. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shibe.online API returns.

## Native endpoint

Through the native Shibe.online API, this operation is `GET /api/cats` (base URL `https://shibe.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-cat-images.md) for the provider-specific parameters and requirements.

