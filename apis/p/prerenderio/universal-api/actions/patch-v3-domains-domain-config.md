# Prerender.io: Update Domains Config

Updates config for a domain in Prerender.io.

```
PUT https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/patch-v3-domains-domain-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/patch-v3-domains-domain-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cacheLifetimeHours": 1,
  "domain": "string",
  "onlyServeCacheHits": true,
  "slowRenderTriggerSeconds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/patch-v3-domains-domain-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cacheLifetimeHours": 1,
    "domain": "string",
    "onlyServeCacheHits": true,
    "slowRenderTriggerSeconds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cacheLifetimeHours` | number | yes |  |
| `domain` | string | yes |  |
| `onlyServeCacheHits` | boolean | yes |  |
| `slowRenderTriggerSeconds` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avgCacheMinutes": 1,
      "bandwidthAllowed": 1,
      "bandwidthUsed": 1,
      "cacheLifetimeHours": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "numCacheToday": 1,
      "onlyServeCacheHits": true,
      "pagesCount": 1,
      "slowRenderLinkCount": 1,
      "slowRenderTriggerSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avgCacheMinutes` | number |  |
| `bandwidthAllowed` | number |  |
| `bandwidthUsed` | number |  |
| `cacheLifetimeHours` | number |  |
| `createdAt` | date |  |
| `numCacheToday` | number |  |
| `onlyServeCacheHits` | boolean |  |
| `pagesCount` | number |  |
| `slowRenderLinkCount` | number |  |
| `slowRenderTriggerSeconds` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `PATCH /v3/domains/{domain}/config` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-v3-domains-domain-config.md) for the provider-specific parameters and requirements.

