# Payrexx: Create Paylink

Creates a paylink in Payrexx.

```
POST https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-paylink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-paylink" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "description": "string",
  "referenceId": "string",
  "purpose": "string",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-paylink', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "description": "string",
    "referenceId": "string",
    "purpose": "string",
    "amount": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Page title shown on the payment page. |
| `description` | string | yes | Description shown on the payment page. |
| `referenceId` | string | yes | Internal reference id used by your system. |
| `purpose` | string | yes | Purpose of the payment. |
| `amount` | number | yes | Amount in cents. |
| `currency` | string | yes | Currency code for the payment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `POST Invoice/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-paylink.md) for the provider-specific parameters and requirements.

