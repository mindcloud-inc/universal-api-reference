# Dwolla: Create Transfer

Creates a new transfer in Dwolla.

```
POST https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/create-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/create-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "_links.source.href": "https://example.com",
  "_links.destination.href": "https://example.com",
  "amount.currency": "USD",
  "amount.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/create-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "_links.source.href": "https://example.com",
    "_links.destination.href": "https://example.com",
    "amount.currency": "USD",
    "amount.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `_links.source.href` | string | yes | Source funding source URL |
| `_links.destination.href` | string | yes | Destination funding source URL |
| `amount.currency` | string | yes | Transfer currency Default: `USD`. |
| `amount.value` | string | yes | Transfer amount value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dwolla API returns.

## Native endpoint

Through the native Dwolla API, this operation is `POST /transfers` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transfer.md) for the provider-specific parameters and requirements.

