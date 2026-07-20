# Scrape do: Send PUT request

Sends a PUT request with Scrape do.

```
PUT https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/send-put-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/send-put-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/send-put-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The target URL that will receive the PUT request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrape do API returns.

## Native endpoint

Through the native Scrape do API, this operation is `PUT /` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-put-request.md) for the provider-specific parameters and requirements.

