# Viewpoint Vista: Add SM Customer

Adds a new SM Customer Record.

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-sm-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-sm-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sMCo": 1,
  "Customer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-sm-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sMCo": 1,
    "Customer": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sMCo` | number | yes |  |
| `Customer` | number | yes | Key to `ar/customer(CustGroup, Customer)`. `CustGroup` is defaulted based on the provided `SMCo`. Customer must already exist in the `ar/customers` endpoint. |
| `active` | list<string> | no | Optional. If omitted, `Y` will be defaulted. |
| `nonBillable` | list<string> | no | Optional. If omitted, `N` will be defaulted. |
| `rateTemplate` | string | no | Key to SM Rate Template. Optional. If omitted, null will be defaulted. |
| `billToARCustomer` | number | no | Alternate Bill To Customer. Optional. Set the Alternate AR Customer to bill to for this SM Customer. If omitted, null will be defaulted. |
| `CustomerPOSetting` | list<string> | no | Optional. If omitted, `N` will be defaulted. Allowed: - `R` - Required - `N` - Not Required |
| `PrimaryTechnician` | string | no | Key to SM Technician. Optional. If omitted, null will be defaulted. |
| `reviewer` | string | no | Key to `hq/reviewers(Reviewer)`. Optional. If omitted, null will be defaulted. |
| `InvoiceGrouping` | list<string> | no | Optional. Allowed: - `C`-One per Customer, - `S`-One per service site - `W`-One per work order - `P`-One per work order scope. If omitted, `C` will be defaulted. |
| `InvoiceGroupingPOOverride` | list<string> | no | Optional. If omitted, `N` will be defaulted. |
| `invoiceSummaryLevel` | string | no | Optional. If omitted, `T-Transaction` will be defaulted. Options: - `L-Line Type` - `C-Cost Type` - `T-Transaction` |
| `ReportID` | number | no |  |
| `DeliveryTo` | list<string> | no | Invoice Delivery Address Type. Options: - `A` AR Customer - `S` Service Site - `O` Other `S` Service Site can only be provided if the `InvoiceGrouping` != `C` |
| `DeliveryMethod` | list<string> | no | If omitted, `P` will be defaulted. |
| `billingEmail` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingName` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingAddress1` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingAddress2` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingCity` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingState` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingPostalCode` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `BillingCountry` | string | no | If omitted, null will be defaulted. Can only be provided if `DeliveryTo` = 'O'. If provided when `DeliveryTo` is not 'O' the input will be ignored. |
| `Notes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "operation": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `operation` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-sm-customer.md) for the provider-specific parameters and requirements.

