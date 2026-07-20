# ServiceTitan: Get Equipments

Retrieves pricebook equipment from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-equipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-equipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-equipments?${params}`, {
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
| `createdOnOrAfter` | string | no |  |

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
      "assets": [
        {
          "alias": {},
          "fileName": {},
          "isDefault": true,
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "bonus": 1,
      "budgetCostCode": {},
      "budgetCostType": {},
      "categories": [
        1
      ],
      "code": "string",
      "commissionBonus": 1,
      "cost": 1,
      "costOfSaleAccount": "string",
      "createdOn": "string",
      "crossSaleGroup": {},
      "defaultAssetUrl": "https://example.com",
      "description": "string",
      "dimensions": {
        "depth": 1,
        "height": 1,
        "width": 1
      },
      "displayInAmount": true,
      "displayName": "Ava Chen",
      "externalId": {},
      "generalLedgerAccountId": 1,
      "hours": 1,
      "id": 1,
      "isConfigurableEquipment": true,
      "isInventory": true,
      "manufacturer": "string",
      "manufacturerWarranty": {
        "description": {},
        "duration": 1
      },
      "memberPrice": 1,
      "model": "string",
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
      "serviceProviderWarranty": {
        "description": {},
        "duration": 1
      },
      "source": {},
      "taxable": true,
      "typeId": 1,
      "unitOfMeasure": {}
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
| `assets[].alias` | object |  |
| `assets[].fileName` | object |  |
| `assets[].isDefault` | boolean |  |
| `assets[].type` | string |  |
| `assets[].url` | string |  |
| `bonus` | number |  |
| `budgetCostCode` | object |  |
| `budgetCostType` | object |  |
| `categories[]` | number |  |
| `code` | string |  |
| `commissionBonus` | number |  |
| `cost` | number |  |
| `costOfSaleAccount` | string |  |
| `createdOn` | string |  |
| `crossSaleGroup` | object |  |
| `defaultAssetUrl` | string |  |
| `description` | string |  |
| `dimensions.depth` | number |  |
| `dimensions.height` | number |  |
| `dimensions.width` | number |  |
| `displayInAmount` | boolean |  |
| `displayName` | string |  |
| `externalId` | object |  |
| `generalLedgerAccountId` | number |  |
| `hours` | number |  |
| `id` | number |  |
| `isConfigurableEquipment` | boolean |  |
| `isInventory` | boolean |  |
| `manufacturer` | string |  |
| `manufacturerWarranty.description` | object |  |
| `manufacturerWarranty.duration` | number |  |
| `memberPrice` | number |  |
| `model` | string |  |
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
| `serviceProviderWarranty.description` | object |  |
| `serviceProviderWarranty.duration` | number |  |
| `source` | object |  |
| `taxable` | boolean |  |
| `typeId` | number |  |
| `unitOfMeasure` | object |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET pricebook/v2/tenant/{{credentials.tenant}}/equipment` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-equipments.md) for the provider-specific parameters and requirements.

