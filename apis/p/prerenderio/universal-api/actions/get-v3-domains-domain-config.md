# Prerender.io: Get Domains Config

Retrieves config for a domain from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domains-domain-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domains-domain-config?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domains-domain-config?${params}`, {
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
| `domain` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avgCacheMinutes": 1,
      "cacheLifetimeHours": 1,
      "createdAt": "string",
      "numberOfNotCached": 1,
      "numCache_g1l7": 1,
      "numCache_g30": 1,
      "numCache_g7l30": 1,
      "numCacheToday": 1,
      "onlyServeCacheHits": true,
      "pagesCount": 1,
      "slowRenderTriggerSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgCacheMinutes` | number |  |
| `cacheLifetimeHours` | number |  |
| `createdAt` | string |  |
| `numberOfNotCached` | number |  |
| `numCache_g1l7` | number |  |
| `numCache_g30` | number |  |
| `numCache_g7l30` | number |  |
| `numCacheToday` | number |  |
| `onlyServeCacheHits` | boolean |  |
| `pagesCount` | number |  |
| `slowRenderTriggerSeconds` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/domains/{domain}/config` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-domains-domain-config.md) for the provider-specific parameters and requirements.

