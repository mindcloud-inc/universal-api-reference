# Viewpoint Spectrum: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerCode` | string | yes | Customer Code. |
| `name` | string | no | Customer Name. |
| `alphaSort` | string | no | Customer Alpha Ref. |
| `type` | string | no | Customer Type. |
| `address1` | string | no | Address 1. |
| `address2` | string | no | Address 2. |
| `city` | string | no | City. |
| `state` | string | no | State. |
| `zipCode` | string | no | Zip Code. |
| `phone` | string | no | Phone Number. |
| `faxPhone` | string | no | Fax number. |
| `contact1` | string | no | Contact 1. |
| `contact2` | string | no | Contact 2. |
| `contact3` | string | no | Contact 3. |
| `salesperson` | string | no | Salesman Code. |
| `termsCode` | string | no | Terms Code. |
| `standardRetentionPercent` | number | no | Default Retention (Holdback) percent. |
| `taxableFlag` | string | no | Taxable flag (Y/N). |
| `salesTaxCode` | string | no | Sales tax code. |
| `resaleNumber` | string | no | Resale certificate number. |
| `resaleExpDate` | date | no | Resale expiration date. |
| `statementFlag` | string | no | Send statement flag (Y/N). |
| `financeChargeTranCode` | string | no | Finance Charge Code. |
| `financeCharge` | number | no | Finance Charge percent. |
| `priceLevelMaterial` | number | no | Work Order Material Level. |
| `priceLevelLabor` | number | no | Work Order Labor Level. |
| `creditLimit` | number | no | Credit Limit. |
| `dateCreated` | date | no | Date Established. |
| `Email1` | string | no | Customer Email. |
| `markupCode` | string | no | Non-stock Markup Code. |
| `userDefinedFields` | object | no | User-defined fields object for UDF1 through UDF20. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddCustomer` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

