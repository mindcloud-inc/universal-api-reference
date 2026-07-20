# Simpro: Create Quote



```
POST https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "0",
  "Type": "string",
  "Site": 1,
  "Customer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "0",
    "Type": "string",
    "Site": 1,
    "Customer": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Default: `0`. |
| `Type` | string | yes |  |
| `Site` | number | yes |  |
| `Customer` | number | yes |  |
| `Description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoAdjustStatus": true,
      "convertedFromLead": {},
      "customer": {
        "companyName": "Ava Chen",
        "familyName": "Ava Chen",
        "givenName": "Ava Chen",
        "id": 1
      },
      "customerContact": {},
      "customerContract": {
        "contractNo": "string",
        "endDate": "string",
        "id": 1,
        "name": "Ava Chen",
        "startDate": "string"
      },
      "customerStage": "string",
      "dateApproved": "string",
      "dateIssued": "string",
      "dateModified": "string",
      "description": "string",
      "dueDate": {},
      "forecast": {
        "month": {},
        "percent": 1,
        "year": {}
      },
      "id": 1,
      "isClosed": true,
      "isVariation": true,
      "jobNo": {},
      "linkedJobID": {},
      "name": "Ava Chen",
      "notes": "string",
      "orderNo": "string",
      "projectManager": {},
      "requestNo": "string",
      "salesperson": {},
      "site": {
        "id": 1,
        "name": "Ava Chen"
      },
      "siteContact": {},
      "stage": "string",
      "status": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "stc": {
        "sTCsEligible": true,
        "sTCValue": 1,
        "vEECsEligible": true,
        "vEECValue": 1
      },
      "technician": {},
      "total": {
        "exTax": 1,
        "incTax": 1,
        "tax": 1
      },
      "totals": {
        "adjusted": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "discount": 1,
        "grossMargin": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "grossProfitLoss": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "materialsCost": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "materialsMarkup": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "membershipDiscount": 1,
        "nettMargin": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "nettProfitLoss": {
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "resourcesCost": {
          "commission": {
            "estimate": 1,
            "revised": 1
          },
          "labor": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "laborHours": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "overhead": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "plantAndEquipment": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "plantAndEquipmentHours": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "total": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          }
        },
        "resourcesMarkup": {
          "labor": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "plantAndEquipment": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "total": {
            "estimate": 1,
            "revised": 1,
            "revized": 1
          }
        },
        "sTCs": 1,
        "vEECs": 1
      },
      "type": "string",
      "validityDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoAdjustStatus` | boolean |  |
| `convertedFromLead` | object |  |
| `customer.companyName` | string |  |
| `customer.familyName` | string |  |
| `customer.givenName` | string |  |
| `customer.id` | number |  |
| `customerContact` | object |  |
| `customerContract.contractNo` | string |  |
| `customerContract.endDate` | string |  |
| `customerContract.id` | number |  |
| `customerContract.name` | string |  |
| `customerContract.startDate` | string |  |
| `customerStage` | string |  |
| `dateApproved` | string |  |
| `dateIssued` | string |  |
| `dateModified` | string |  |
| `description` | string |  |
| `dueDate` | object |  |
| `forecast.month` | object |  |
| `forecast.percent` | number |  |
| `forecast.year` | object |  |
| `id` | number |  |
| `isClosed` | boolean |  |
| `isVariation` | boolean |  |
| `jobNo` | object |  |
| `linkedJobID` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `orderNo` | string |  |
| `projectManager` | object |  |
| `requestNo` | string |  |
| `salesperson` | object |  |
| `site.id` | number |  |
| `site.name` | string |  |
| `siteContact` | object |  |
| `stage` | string |  |
| `status.color` | string |  |
| `status.id` | number |  |
| `status.name` | string |  |
| `stc.sTCsEligible` | boolean |  |
| `stc.sTCValue` | number |  |
| `stc.vEECsEligible` | boolean |  |
| `stc.vEECValue` | number |  |
| `technician` | object |  |
| `total.exTax` | number |  |
| `total.incTax` | number |  |
| `total.tax` | number |  |
| `totals.adjusted.estimate` | number |  |
| `totals.adjusted.revised` | number |  |
| `totals.adjusted.revized` | number |  |
| `totals.discount` | number |  |
| `totals.grossMargin.estimate` | number |  |
| `totals.grossMargin.revised` | number |  |
| `totals.grossMargin.revized` | number |  |
| `totals.grossProfitLoss.estimate` | number |  |
| `totals.grossProfitLoss.revised` | number |  |
| `totals.grossProfitLoss.revized` | number |  |
| `totals.materialsCost.estimate` | number |  |
| `totals.materialsCost.revised` | number |  |
| `totals.materialsCost.revized` | number |  |
| `totals.materialsMarkup.estimate` | number |  |
| `totals.materialsMarkup.revised` | number |  |
| `totals.materialsMarkup.revized` | number |  |
| `totals.membershipDiscount` | number |  |
| `totals.nettMargin.estimate` | number |  |
| `totals.nettMargin.revised` | number |  |
| `totals.nettMargin.revized` | number |  |
| `totals.nettProfitLoss.estimate` | number |  |
| `totals.nettProfitLoss.revised` | number |  |
| `totals.nettProfitLoss.revized` | number |  |
| `totals.resourcesCost.commission.estimate` | number |  |
| `totals.resourcesCost.commission.revised` | number |  |
| `totals.resourcesCost.labor.estimate` | number |  |
| `totals.resourcesCost.labor.revised` | number |  |
| `totals.resourcesCost.labor.revized` | number |  |
| `totals.resourcesCost.laborHours.estimate` | number |  |
| `totals.resourcesCost.laborHours.revised` | number |  |
| `totals.resourcesCost.laborHours.revized` | number |  |
| `totals.resourcesCost.overhead.estimate` | number |  |
| `totals.resourcesCost.overhead.revised` | number |  |
| `totals.resourcesCost.overhead.revized` | number |  |
| `totals.resourcesCost.plantAndEquipment.estimate` | number |  |
| `totals.resourcesCost.plantAndEquipment.revised` | number |  |
| `totals.resourcesCost.plantAndEquipment.revized` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.estimate` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.revised` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.revized` | number |  |
| `totals.resourcesCost.total.estimate` | number |  |
| `totals.resourcesCost.total.revised` | number |  |
| `totals.resourcesCost.total.revized` | number |  |
| `totals.resourcesMarkup.labor.estimate` | number |  |
| `totals.resourcesMarkup.labor.revised` | number |  |
| `totals.resourcesMarkup.labor.revized` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.estimate` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.revised` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.revized` | number |  |
| `totals.resourcesMarkup.total.estimate` | number |  |
| `totals.resourcesMarkup.total.revised` | number |  |
| `totals.resourcesMarkup.total.revized` | number |  |
| `totals.sTCs` | number |  |
| `totals.vEECs` | number |  |
| `type` | string |  |
| `validityDays` | number |  |

## Native endpoint

Through the native Simpro API, this operation is `POST /companies/:companyId/quotes/` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

