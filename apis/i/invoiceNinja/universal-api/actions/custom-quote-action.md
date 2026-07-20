# Invoice Ninja: Custom Quote Action



```
PUT https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/custom-quote-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/custom-quote-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quoteId": "string",
  "quoteAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/custom-quote-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quoteId": "string",
    "quoteAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | string | yes | Hashed quote ID. |
| `quoteAction` | string | yes | Deprecated per-quote action string, such as history, archive, convert_to_invoice, or download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Invoice Ninja API returns.

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /quotes/:id/:action` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/custom-quote-action.md) for the provider-specific parameters and requirements.

