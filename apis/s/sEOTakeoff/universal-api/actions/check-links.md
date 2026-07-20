# SEOTakeoff: Check Links



```
GET https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/check-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/check-links?connectionId=$CONNECTION_ID&urls%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urls[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/check-links?${params}`, {
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
| `urls[]` | array<string> | yes | List of URLs to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "ok": true,
      "redirect_url": "https://example.com",
      "status_code": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `ok` | boolean |  |
| `redirect_url` | string |  |
| `status_code` | number |  |
| `url` | string |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/v1/tools/check-links` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-links.md) for the provider-specific parameters and requirements.

