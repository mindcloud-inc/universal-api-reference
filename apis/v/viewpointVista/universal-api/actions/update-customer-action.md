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
| `BillingAddress.BillAddress` | string | no | Billing address line 1 (max 60). |
| `BillingAddress.BillAddress2` | string | no | Billing address line 2 (max 60). |
| `BillingAddress.BillCity` | string | no | Billing city (max 30). |
| `BillingAddress.BillCountry` | string | no | Billing country code (2 letters, e.g. US). |
| `BillingAddress.BillState` | string | no | Billing state (max 4). Validated by Vista against the states of the BillCountry. |
| `BillingAddress.BillZip` | string | no | Billing ZIP / postal code (max 12). |
| `CompanyContact.Phone` | string | no |  |
| `MailingAddress.Address` | string | no | Mailing address line 1 (max 60). |
| `MailingAddress.Address2` | string | no | Mailing address line 2 (max 60). |
| `MailingAddress.City` | string | no | Mailing city (max 30). |
| `MailingAddress.Country` | string | no | Mailing country code (2 letters, e.g. US). |
| `MailingAddress.State` | string | no | Mailing state (max 4). Validated by Vista against the states of the Country. |
| `MailingAddress.Zip` | string | no | Mailing ZIP / postal code (max 12). |
| `CompanyContact.Fax` | string | no |  |
| `Name` | string | no |  |
| `CompanyContact.Contact` | string | no |  |
| `RecType` | number | no | Receivable Type key for the AR company. Optional; Vista uses the company default when omitted. |
| `CompanyContact.ContactExt` | string | no |  |
| `MailingAddress` | object | no |  |
| `BillingAddress` | object | no |  |
| `CompanyContact.EMail` | string | no |  |
| `CompanyContact.URL` | string | no |  |
| `PayTerms` | string | no |  |
| `TaxCode` | string | no |  |
| `CompanyContact` | object | no |  |
| `__key` | object | no | Identifies the customer to change. Required. Use exactly one of two forms: { "KeyID": 12345 } (surrogate key) or { "CustGroup": 1, "Customer": 1001 } (natural key; CustGroup must match the one of the ARCo in HQ company parameters). Each form accepts only its own properties. |
| `__custom_fields` | object | no |  |
| `SortName` | string | no | New customer sort name (max 15 characters). Only sent properties are changed. |
| `Status` | string | no | New customer status: A = Active, I = Inactive, H = On Hold. Only sent properties are changed. |
| `DateOpened` | string | no | New date opened, in YYYY-MM-DD format (date only, no time). Only sent properties are changed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/change` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-action.md) for the provider-specific parameters and requirements.

