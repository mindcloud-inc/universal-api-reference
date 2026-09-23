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
  "Customer_Code": "string",
  "Name": "Ava Chen"
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
    "Customer_Code": "string",
    "Name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Address_1` | string | no |  |
| `Address_2` | string | no |  |
| `alphaSort` | string | no |  |
| `City` | string | no |  |
| `Customer_Code` | string | yes |  |
| `Name` | string | yes |  |
| `type` | string | no |  |
| `State` | string | no |  |
| `Zip_Code` | string | no |  |
| `Phone_Number` | string | no |  |
| `faxPhone` | string | no |  |
| `contact1` | string | no |  |
| `contact2` | string | no |  |
| `contact3` | string | no |  |
| `salesperson` | string | no |  |
| `standardRetentionPercent` | number | no |  |
| `Taxable_Flag` | list | no |  |
| `resaleNumber` | string | no |  |
| `resaleExpDate` | date | no |  |
| `Statement_Flag` | list | no |  |
| `financeChargeTranCode` | string | no |  |
| `financeCharge` | number | no |  |
| `priceLevelMaterial` | list<number> | no |  |
| `priceLevelLabor` | list<number> | no |  |
| `creditLimit` | number | no |  |
| `dateCreated` | date | no |  |
| `Email1` | string | no |  |
| `markupCode` | string | no |  |
| `userDefinedFields` | object | no | UDF1 — UDF20 |
| `Terms_Code` | string | no |  |
| `Sales_Tax_Code` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST customer/updatecustomer` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

