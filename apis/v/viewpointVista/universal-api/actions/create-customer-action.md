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
| `BillingAddress.BillAddress` | string | no | Billing address line 1 (max 60). |
| `BillingAddress.BillAddress2` | string | no | Billing address line 2 (max 60). |
| `BillingAddress.BillCity` | string | no | Billing city (max 30). |
| `BillingAddress.BillCountry` | string | no | Billing country code (2 letters, e.g. US). Defaults to the HQ company default country. |
| `BillingAddress.BillState` | string | no | Billing state (max 4). Validated by Vista against the states of the BillCountry. |
| `BillingAddress.BillZip` | string | no | Billing ZIP / postal code (max 12). |
| `CompanyContact.Contact` | string | no | Contact name (max 30). |
| `CompanyContact.ContactExt` | string | no | Contact phone extension (max 10). |
| `CompanyContact.EMail` | string | no | Contact email (max 255). |
| `CompanyContact.Fax` | string | no | Contact fax (max 20). |
| `CompanyContact.Phone` | string | no | Contact phone (max 20). |
| `CompanyContact.URL` | string | no | Contact website URL (max 60). |
| `MailingAddress.Address` | string | no | Mailing address line 1 (max 60). |
| `MailingAddress.Address2` | string | no | Mailing address line 2 (max 60). |
| `MailingAddress.City` | string | no | Mailing city (max 30). |
| `MailingAddress.Country` | string | no | Mailing country code (2 letters, e.g. US). Defaults to the HQ company default country. |
| `MailingAddress.State` | string | no | Mailing state (max 4). Validated by Vista against the states of the Country. |
| `MailingAddress.Zip` | string | no | Mailing ZIP / postal code (max 12). |
| `Customer` | object | no |  |
| `Name` | string | no |  |
| `RecType` | number | no | Receivable Type key for the AR company. Optional; Vista uses the company default when omitted. |
| `MailingAddress` | object | no |  |
| `BillingAddress` | object | no |  |
| `PayTerms` | string | no |  |
| `CompanyContact` | object | no |  |
| `__custom_fields` | object | no |  |
| `TaxCode` | string | no |  |
| `SortName` | string | no | Customer sort name (max 15 characters). If omitted, Vista calculates it from the name and appends trailing digits when the result is not unique. |
| `Status` | string | no | Customer status: A = Active, I = Inactive, H = On Hold. Defaults to A when omitted. |
| `DateOpened` | string | no | Date the customer was opened, in YYYY-MM-DD format (date only, no time). Defaults to today's date when omitted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-action.md) for the provider-specific parameters and requirements.

