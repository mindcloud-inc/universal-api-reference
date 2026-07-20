# RealFaviconGenerator: Start favicon generation



```
POST https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/start-favicon-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RealFaviconGenerator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/start-favicon-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/start-favicon-generation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `masterPictureType` | list | no | How the master favicon picture is supplied: no picture, URL, or inline Base64 content. One of: `inline`, `no_picture`, `url`. Default: `no_picture`. |
| `masterPictureUrl` | string | no | URL of the source image when Master picture type is url. Example: `https://example.com/logo.png`. |
| `demo` | boolean | no | When no master picture is supplied, show RealFaviconGenerator's demo option. Default: `false`. |
| `filesLocationType` | list | no | How the favicon file deployment location is chosen. One of: `no_location`, `path`, `root`. Default: `no_location`. |
| `filesLocationPath` | string | no | Deployment path when Files location type is path, such as /assets/icons. Example: `/assets/icons`. |
| `callbackType` | list | no | Whether RealFaviconGenerator redirects to a callback URL or lets the user download directly. One of: `none`, `url`. Default: `none`. |
| `callbackUrl` | string | no | URL RealFaviconGenerator redirects to after generation when Callback type is url. Example: `https://example.com/rfg-callback`. |
| `shortUrl` | boolean | no | Return a json_result_url callback instead of embedding the JSON result in the callback URL. Default: `false`. |
| `pathOnly` | boolean | no | When short callback URLs are enabled, return only a path so the receiver can prepend the RealFaviconGenerator host. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `masterPictureContent` | string | no | Base64-encoded image content when Master picture type is inline. |
| `customParameter` | string | no | Custom query-string fragment returned to the callback URL, such as ref=157539001. Example: `ref=157539001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RealFaviconGenerator API returns.

## Native endpoint

Through the native RealFaviconGenerator API, this operation is `GET /favicon_generator` (base URL `https://realfavicongenerator.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-favicon-generation.md) for the provider-specific parameters and requirements.

