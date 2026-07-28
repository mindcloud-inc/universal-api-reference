# Viewpoint Vista: Create Customer Action



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-customer-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-customer-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/create-customer-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ARCo` | number | no |  |
| `Customer` | object | no |  |
| `Name` | string | no |  |
| `MailingAddress` | object | no |  |
| `BillingAddress` | object | no |  |
| `PayTerms` | string | no |  |
| `CompanyContact` | object | no |  |
| `__custom_fields` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-action.md) for the provider-specific parameters and requirements.

