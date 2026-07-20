# Evoliz: Send Quote

Sends a quote by email from Evoliz.

```
PUT https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/send-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/send-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quoteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/send-quote', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quoteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | number | yes | The Evoliz quote ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Evoliz API returns.

## Native endpoint

Through the native Evoliz API, this operation is `POST /api/v1/quotes/:quoteid/send` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-quote.md) for the provider-specific parameters and requirements.

