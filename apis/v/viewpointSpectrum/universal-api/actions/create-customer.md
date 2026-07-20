# Viewpoint Spectrum: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address1` | string | no |  |
| `address2` | string | no |  |
| `alphaSort` | string | no |  |
| `city` | string | no |  |
| `customerCode` | string | yes |  |
| `name` | string | yes |  |
| `type` | string | no |  |
| `state` | string | no |  |
| `zipCode` | string | no |  |
| `phone` | string | no |  |
| `faxPhone` | string | no |  |
| `contact1` | string | no |  |
| `contact2` | string | no |  |
| `contact3` | string | no |  |
| `salesperson` | string | no |  |
| `termsCode` | string | no | Default: `NET30`. |
| `standardRetentionPercent` | number | no |  |
| `taxableFlag` | list | no |  |
| `salesTaxCode` | string | no |  |
| `resaleNumber` | string | no |  |
| `resaleExpDate` | date | no |  |
| `statementFlag` | list | no |  |
| `financeChargeTranCode` | string | no |  |
| `financeCharge` | number | no |  |
| `priceLevelMaterial` | list<number> | no |  |
| `priceLevelLabor` | list<number> | no |  |
| `creditLimit` | number | no |  |
| `dateCreated` | date | no |  |
| `customerEmail` | string | no |  |
| `markupCode` | string | no |  |
| `userDefinedFields` | object | no | UDF1 — UDF20 |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddCustomer` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

