# ScrapeOps: List Browser Headers

Retrieves fake browser headers from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-browser-headers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-browser-headers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-browser-headers?${params}`, {
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
| `numResults` | number | no | How many browser headers to return |
| `mobile` | boolean | no | Return mobile browser headers only when true |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept": "string",
      "acceptEncoding": "string",
      "acceptLanguage": "string",
      "secChUa": "string",
      "secChUaMobile": "string",
      "secChUaPlatform": "string",
      "secFetchDest": "string",
      "secFetchMode": "string",
      "secFetchSite": "string",
      "secFetchUser": "string",
      "upgradeInsecureRequests": "string",
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accept` | string |  |
| `acceptEncoding` | string |  |
| `acceptLanguage` | string |  |
| `secChUa` | string |  |
| `secChUaMobile` | string |  |
| `secChUaPlatform` | string |  |
| `secFetchDest` | string |  |
| `secFetchMode` | string |  |
| `secFetchSite` | string |  |
| `secFetchUser` | string |  |
| `upgradeInsecureRequests` | string |  |
| `userAgent` | string |  |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET /browser-headers` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-browser-headers.md) for the provider-specific parameters and requirements.

