# SuperSend: Purchase Domains and Mailboxes

Creates managed domains and mailboxes in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/purchase-domains-and-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/purchase-domains-and-mailboxes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentMethodId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/purchase-domains-and-mailboxes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentMethodId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domains[]` | array<string> | no |  |
| `domainsWithProviders[]` | array<object> | no |  |
| `domainsWithProviders[].domain` | string | no |  |
| `domainsWithProviders[].provider` | string | no | Allowed values: google, outlook, smtp. |
| `mailboxes[]` | array<object> | no |  |
| `mailboxes[].username` | string | no |  |
| `mailboxes[].firstName` | string | no |  |
| `mailboxes[].lastName` | string | no |  |
| `mailboxes[].domain` | string | no |  |
| `mailboxes[].signature` | string | no |  |
| `mailboxes[].provider` | string | no | Allowed values: google, outlook, smtp. |
| `paymentMethodId` | string | yes |  |
| `teamId` | string | no |  |
| `forwardingAddress` | string | no |  |
| `dmarcEmail` | string | no |  |
| `contactDetails` | object | no |  |
| `saveContactAsDefault` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SuperSend API returns.

## Native endpoint

Through the native SuperSend API, this operation is `POST /domains/purchase-with-mailboxes` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-domains-and-mailboxes.md) for the provider-specific parameters and requirements.

