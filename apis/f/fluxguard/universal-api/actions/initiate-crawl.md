# Fluxguard: Initiate Crawl

Initiates a crawl for a Fluxguard monitoring session.

```
POST https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/initiate-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/initiate-crawl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/initiate-crawl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes |  |
| `sessionId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fluxguard API returns.

## Native endpoint

Through the native Fluxguard API, this operation is `POST /site/:siteId/session/:sessionId/crawl` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-crawl.md) for the provider-specific parameters and requirements.

