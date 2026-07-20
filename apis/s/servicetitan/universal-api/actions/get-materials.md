# ServiceTitan: Get Materials

Retrieves pricebook materials from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-materials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-materials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-materials?${params}`, {
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
| `modifiedOnOrAfter` | string | no |  |
| `createdOnOrAfter` | string | no | Format - date-time (as date-time in RFC3339). Return items created on or after certain date/time (in UTC) |
| `sort` | string | no | Applies sorting by the specified field: "?sort=+FieldName" for ascending order, "?sort=-FieldName" for descending order. Available fields are: Id, Code, DisplayName, CreatedOn, ModifiedOn, Price, MemberPrice, AddOnPrice, AddOnMemberPrice, MaterialsCost, PrimaryVendor, Cost, Manufacturer, Priority. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "active": true,
      "addOnMemberPrice": 1,
      "addOnPrice": 1,
      "assetAccount": {},
      "bonus": 1,
      "budgetCostCode": {},
      "budgetCostType": {},
      "businessUnitId": {},
      "categories": [
        1
      ],
      "chargeableByDefault": true,
      "code": "string",
      "commissionBonus": 1,
      "cost": 1,
      "costOfSaleAccount": "string",
      "costTypeId": {},
      "createdById": 1,
      "createdOn": "string",
      "deductAsJobCost": true,
      "defaultAssetUrl": {},
      "description": "string",
      "displayInAmount": true,
      "displayName": "Ava Chen",
      "externalId": {},
      "generalLedgerAccountId": 1,
      "hours": 1,
      "id": 1,
      "isConfigurableMaterial": true,
      "isInventory": true,
      "isOtherDirectCost": true,
      "memberPrice": 1,
      "modifiedOn": "string",
      "otherVendors": [
        {
          "active": true,
          "cost": 1,
          "id": 1,
          "memo": {},
          "primarySubAccount": {},
          "vendorId": 1,
          "vendorName": "Ava Chen",
          "vendorPart": {}
        }
      ],
      "paysCommission": true,
      "price": 1,
      "primaryVendor": {
        "active": true,
        "cost": 1,
        "id": 1,
        "memo": {},
        "primarySubAccount": {},
        "vendorId": 1,
        "vendorName": "Ava Chen",
        "vendorPart": {}
      },
      "source": {},
      "taxable": true,
      "unitOfMeasure": {},
      "variationsOrConfigurableMaterials": [
        1
      ]
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
| `addOnMemberPrice` | number |  |
| `addOnPrice` | number |  |
| `assetAccount` | object |  |
| `bonus` | number |  |
| `budgetCostCode` | object |  |
| `budgetCostType` | object |  |
| `businessUnitId` | object |  |
| `categories[]` | number |  |
| `chargeableByDefault` | boolean |  |
| `code` | string |  |
| `commissionBonus` | number |  |
| `cost` | number |  |
| `costOfSaleAccount` | string |  |
| `costTypeId` | object |  |
| `createdById` | number |  |
| `createdOn` | string |  |
| `deductAsJobCost` | boolean |  |
| `defaultAssetUrl` | object |  |
| `description` | string |  |
| `displayInAmount` | boolean |  |
| `displayName` | string |  |
| `externalId` | object |  |
| `generalLedgerAccountId` | number |  |
| `hours` | number |  |
| `id` | number |  |
| `isConfigurableMaterial` | boolean |  |
| `isInventory` | boolean |  |
| `isOtherDirectCost` | boolean |  |
| `memberPrice` | number |  |
| `modifiedOn` | string |  |
| `otherVendors[].active` | boolean |  |
| `otherVendors[].cost` | number |  |
| `otherVendors[].id` | number |  |
| `otherVendors[].memo` | object |  |
| `otherVendors[].primarySubAccount` | object |  |
| `otherVendors[].vendorId` | number |  |
| `otherVendors[].vendorName` | string |  |
| `otherVendors[].vendorPart` | object |  |
| `paysCommission` | boolean |  |
| `price` | number |  |
| `primaryVendor.active` | boolean |  |
| `primaryVendor.cost` | number |  |
| `primaryVendor.id` | number |  |
| `primaryVendor.memo` | object |  |
| `primaryVendor.primarySubAccount` | object |  |
| `primaryVendor.vendorId` | number |  |
| `primaryVendor.vendorName` | string |  |
| `primaryVendor.vendorPart` | object |  |
| `source` | object |  |
| `taxable` | boolean |  |
| `unitOfMeasure` | object |  |
| `variationsOrConfigurableMaterials[]` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET pricebook/v2/tenant/{{credentials.tenant}}/materials` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-materials.md) for the provider-specific parameters and requirements.

