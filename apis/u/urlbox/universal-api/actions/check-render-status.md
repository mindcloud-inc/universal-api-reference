# Urlbox: Check Render Status

Retrieves the status of a render from Urlbox.

```
GET https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/check-render-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Urlbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/check-render-status?connectionId=$CONNECTION_ID&renderId=250ea007-552c-4555-ba2b-ef1c73e18be2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "renderId": "250ea007-552c-4555-ba2b-ef1c73e18be2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/check-render-status?${params}`, {
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
| `renderId` | string | yes | The render ID returned by the async render action Example: `250ea007-552c-4555-ba2b-ef1c73e18be2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bandwidth": 1,
      "queueTime": 1,
      "reason": "string",
      "renderId": "string",
      "renderTime": 1,
      "renderUrl": "https://example.com",
      "size": 1,
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bandwidth` | number | Bandwidth used for the generated render in bytes when available. |
| `queueTime` | number | Time spent waiting in queue in milliseconds when available. |
| `reason` | string | Human-readable failure reason when the render fails. |
| `renderId` | string | Identifier for the render request. |
| `renderTime` | number | Render generation time in milliseconds when available. |
| `renderUrl` | string | Generated render URL when the render succeeds. |
| `size` | number | Size of the generated render in bytes when available. |
| `status` | string | Current render status value. |
| `statusUrl` | string | Polling URL for the current render status. |

## Native endpoint

Through the native Urlbox API, this operation is `GET /v1/render/:renderId` (base URL `https://api.urlbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-render-status.md) for the provider-specific parameters and requirements.

