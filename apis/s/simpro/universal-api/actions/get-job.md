# Simpro: Get Job



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-job?connectionId=$CONNECTION_ID&companyId=0&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0",
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-job?${params}`, {
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
| `companyId` | number | yes | Default: `0`. |
| `jobId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archiveReason": {},
      "autoAdjustStatus": true,
      "completedDate": {},
      "convertedFrom": {},
      "convertedFromQuote": {},
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
      "dateIssued": "string",
      "dateModified": "string",
      "description": "string",
      "dueDate": {},
      "dueTime": {},
      "id": 1,
      "isRetentionEnabled": true,
      "isVariation": true,
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
          "actual": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "discount": 1,
        "grossMargin": {
          "actual": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "grossProfitLoss": {
          "actual": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "invoicedValue": 1,
        "invoicePercentage": 1,
        "materialsCost": {
          "actual": 1,
          "committed": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "materialsMarkup": {
          "actual": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "membershipDiscount": 1,
        "nettMargin": {
          "actual": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "nettProfitLoss": {
          "actual": 1,
          "estimate": 1,
          "revised": 1,
          "revized": 1
        },
        "resourcesCost": {
          "commission": {
            "actual": 1,
            "estimate": 1,
            "revised": 1
          },
          "labor": {
            "actual": 1,
            "committed": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "laborHours": {
            "actual": 1,
            "committed": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "overhead": {
            "actual": 1,
            "committed": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "plantAndEquipment": {
            "actual": 1,
            "committed": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "plantAndEquipmentHours": {
            "actual": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "total": {
            "actual": 1,
            "committed": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          }
        },
        "resourcesMarkup": {
          "labor": {
            "actual": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "plantAndEquipment": {
            "actual": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          },
          "total": {
            "actual": 1,
            "estimate": 1,
            "revised": 1,
            "revized": 1
          }
        },
        "sTCs": 1,
        "vEECs": 1
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archiveReason` | object |  |
| `autoAdjustStatus` | boolean |  |
| `completedDate` | object |  |
| `convertedFrom` | object |  |
| `convertedFromQuote` | object |  |
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
| `dateIssued` | string |  |
| `dateModified` | string |  |
| `description` | string |  |
| `dueDate` | object |  |
| `dueTime` | object |  |
| `id` | number |  |
| `isRetentionEnabled` | boolean |  |
| `isVariation` | boolean |  |
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
| `totals.adjusted.actual` | number |  |
| `totals.adjusted.estimate` | number |  |
| `totals.adjusted.revised` | number |  |
| `totals.adjusted.revized` | number |  |
| `totals.discount` | number |  |
| `totals.grossMargin.actual` | number |  |
| `totals.grossMargin.estimate` | number |  |
| `totals.grossMargin.revised` | number |  |
| `totals.grossMargin.revized` | number |  |
| `totals.grossProfitLoss.actual` | number |  |
| `totals.grossProfitLoss.estimate` | number |  |
| `totals.grossProfitLoss.revised` | number |  |
| `totals.grossProfitLoss.revized` | number |  |
| `totals.invoicedValue` | number |  |
| `totals.invoicePercentage` | number |  |
| `totals.materialsCost.actual` | number |  |
| `totals.materialsCost.committed` | number |  |
| `totals.materialsCost.estimate` | number |  |
| `totals.materialsCost.revised` | number |  |
| `totals.materialsCost.revized` | number |  |
| `totals.materialsMarkup.actual` | number |  |
| `totals.materialsMarkup.estimate` | number |  |
| `totals.materialsMarkup.revised` | number |  |
| `totals.materialsMarkup.revized` | number |  |
| `totals.membershipDiscount` | number |  |
| `totals.nettMargin.actual` | number |  |
| `totals.nettMargin.estimate` | number |  |
| `totals.nettMargin.revised` | number |  |
| `totals.nettMargin.revized` | number |  |
| `totals.nettProfitLoss.actual` | number |  |
| `totals.nettProfitLoss.estimate` | number |  |
| `totals.nettProfitLoss.revised` | number |  |
| `totals.nettProfitLoss.revized` | number |  |
| `totals.resourcesCost.commission.actual` | number |  |
| `totals.resourcesCost.commission.estimate` | number |  |
| `totals.resourcesCost.commission.revised` | number |  |
| `totals.resourcesCost.labor.actual` | number |  |
| `totals.resourcesCost.labor.committed` | number |  |
| `totals.resourcesCost.labor.estimate` | number |  |
| `totals.resourcesCost.labor.revised` | number |  |
| `totals.resourcesCost.labor.revized` | number |  |
| `totals.resourcesCost.laborHours.actual` | number |  |
| `totals.resourcesCost.laborHours.committed` | number |  |
| `totals.resourcesCost.laborHours.estimate` | number |  |
| `totals.resourcesCost.laborHours.revised` | number |  |
| `totals.resourcesCost.laborHours.revized` | number |  |
| `totals.resourcesCost.overhead.actual` | number |  |
| `totals.resourcesCost.overhead.committed` | number |  |
| `totals.resourcesCost.overhead.estimate` | number |  |
| `totals.resourcesCost.overhead.revised` | number |  |
| `totals.resourcesCost.overhead.revized` | number |  |
| `totals.resourcesCost.plantAndEquipment.actual` | number |  |
| `totals.resourcesCost.plantAndEquipment.committed` | number |  |
| `totals.resourcesCost.plantAndEquipment.estimate` | number |  |
| `totals.resourcesCost.plantAndEquipment.revised` | number |  |
| `totals.resourcesCost.plantAndEquipment.revized` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.actual` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.estimate` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.revised` | number |  |
| `totals.resourcesCost.plantAndEquipmentHours.revized` | number |  |
| `totals.resourcesCost.total.actual` | number |  |
| `totals.resourcesCost.total.committed` | number |  |
| `totals.resourcesCost.total.estimate` | number |  |
| `totals.resourcesCost.total.revised` | number |  |
| `totals.resourcesCost.total.revized` | number |  |
| `totals.resourcesMarkup.labor.actual` | number |  |
| `totals.resourcesMarkup.labor.estimate` | number |  |
| `totals.resourcesMarkup.labor.revised` | number |  |
| `totals.resourcesMarkup.labor.revized` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.actual` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.estimate` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.revised` | number |  |
| `totals.resourcesMarkup.plantAndEquipment.revized` | number |  |
| `totals.resourcesMarkup.total.actual` | number |  |
| `totals.resourcesMarkup.total.estimate` | number |  |
| `totals.resourcesMarkup.total.revised` | number |  |
| `totals.resourcesMarkup.total.revized` | number |  |
| `totals.sTCs` | number |  |
| `totals.vEECs` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/jobs/:jobId` (base URL `{{credentials.buildUrl}}/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

