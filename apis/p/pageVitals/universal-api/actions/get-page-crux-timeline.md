# PageVitals: Get Page CrUX Timeline



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-crux-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-crux-timeline?connectionId=$CONNECTION_ID&websiteId=string&pageId=string&device=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "pageId": "string",
  "device": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-crux-timeline?${params}`, {
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
| `websiteId` | string | yes |  |
| `pageId` | string | yes |  |
| `device` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cls": 1,
      "count": 1,
      "date": "string",
      "fcp": 1,
      "fid": 1,
      "inp": 1,
      "lcp": 1,
      "passed": 1,
      "rtt": 1,
      "ttfb": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cls` | number |  |
| `count` | number |  |
| `date` | string |  |
| `fcp` | number |  |
| `fid` | number |  |
| `inp` | number |  |
| `lcp` | number |  |
| `passed` | number |  |
| `rtt` | number |  |
| `ttfb` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/pages/:pageId/crux` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-crux-timeline.md) for the provider-specific parameters and requirements.

