# Billforward: Add Credit To Account

Creates a new credit note for a Billforward account.

```
POST https://connect.mindcloud.co/v1/universal/billforward/latest/actions/add-credit-to-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billforward `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billforward/latest/actions/add-credit-to-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "description": "string",
  "value": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billforward/latest/actions/add-credit-to-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "description": "string",
    "value": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | The Billforward account ID to credit. |
| `description` | string | yes | Credit note description. |
| `value` | number | yes | Credit note value. |
| `currency` | string | yes | Credit note currency code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billforward API returns.

## Native endpoint

Through the native Billforward API, this operation is `POST /accounts/:accountId/credit` (base URL `https://app-sandbox.billforward.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-credit-to-account.md) for the provider-specific parameters and requirements.

