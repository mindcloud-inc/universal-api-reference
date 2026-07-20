# ServiceTitan: Get Discount and Fees

Retrieves pricebook discounts and fees from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-discount-and-fees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-discount-and-fees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-discount-and-fees?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modifiedOnOrAfter` | string | no | Return items modified on or after certain date/time (in UTC) |
| `createdOnOrAfter` | string | no | Return items created on or after certain date/time (in UTC) |
| `sort` | string | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order. Available fields are: Id, Code, DisplayName, CreatedOn, ModifiedOn, Price, MemberPrice, AddOnPrice, AddOnMemberPrice, MaterialsCost, PrimaryVendor, Cost, Manufacturer, Priority. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "active": true,
      "amount": 1,
      "amountType": "string",
      "bonus": 1,
      "budgetCostCode": {},
      "budgetCostType": {},
      "code": "string",
      "commissionBonus": 1,
      "crossSaleGroup": {},
      "description": "string",
      "displayName": "Ava Chen",
      "excludeFromPayroll": true,
      "hours": 1,
      "id": 1,
      "limit": 1,
      "paysCommission": true,
      "taxable": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `active` | boolean |  |
| `amount` | number |  |
| `amountType` | string |  |
| `bonus` | number |  |
| `budgetCostCode` | object |  |
| `budgetCostType` | object |  |
| `code` | string |  |
| `commissionBonus` | number |  |
| `crossSaleGroup` | object |  |
| `description` | string |  |
| `displayName` | string |  |
| `excludeFromPayroll` | boolean |  |
| `hours` | number |  |
| `id` | number |  |
| `limit` | number |  |
| `paysCommission` | boolean |  |
| `taxable` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET pricebook/v2/tenant/{{credentials.tenant}}/discounts-and-fees` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-discount-and-fees.md) for the provider-specific parameters and requirements.

