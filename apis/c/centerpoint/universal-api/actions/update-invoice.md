# Centerpoint: Update Invoice



```
PUT https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "INVOICE_ID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "INVOICE_ID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes` | object | no |  |
| `data.attributes.status` | string | no | Default: `paid`. |
| `INVOICE_ID` | string | yes |  |
| `data` | object | no |  |
| `data.type` | string | no | Default: `invoices`. |
| `data.id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `PATCH invoices/:INVOICE_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

