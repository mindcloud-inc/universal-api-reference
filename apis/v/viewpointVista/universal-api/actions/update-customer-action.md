# Viewpoint Vista: Update Customer Action



```
PUT https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-customer-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-customer-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-customer-action', {
  method: 'PUT',
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
| `CompanyContact.Phone` | string | no |  |
| `CompanyContact.Fax` | string | no |  |
| `Name` | string | no |  |
| `RecType` | number | no | Receivable Type key for the AR company. Optional; Vista uses the company default when omitted. |
| `CompanyContact.Contact` | string | no |  |
| `MailingAddress` | object | no |  |
| `BillingAddress` | object | no |  |
| `CompanyContact.contactExt` | string | no |  |
| `CompanyContact.EMail` | string | no |  |
| `PayTerms` | string | no |  |
| `CompanyContact.URL` | string | no |  |
| `CompanyContact` | object | no |  |
| `__key` | object | no |  |
| `__custom_fields` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/change` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-action.md) for the provider-specific parameters and requirements.

