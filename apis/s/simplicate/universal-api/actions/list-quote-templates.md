# Simplicate: List Quote Templates



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-quote-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-quote-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-quote-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "personId": "string"
      },
      "customerReference": "string",
      "grandTotals": {
        "fixed": {
          "totalExcluding": 1,
          "totalIncluding": 1,
          "totalVat": 1,
          "vatTypes": {
            "21%": 1
          }
        },
        "hours": {
          "totalExcluding": 1,
          "totalIncluding": 1,
          "totalVat": 1,
          "vatTypes": {
            "21%": 1
          }
        }
      },
      "id": "string",
      "isBlocked": true,
      "isOutdated": true,
      "isSepaAuthorization": true,
      "json": "string",
      "lastUpdatedApprovalStatus": "string",
      "paymentTerm": {
        "days": "string",
        "id": "string",
        "method": "string",
        "name": "Ava Chen"
      },
      "quoteDate": "string",
      "quoteNumber": "string",
      "quotestatus": {
        "color": "string",
        "id": "string",
        "label": "string"
      },
      "quoteSubject": "string",
      "quotetemplate": {
        "id": "string",
        "name": "Ava Chen"
      },
      "salesId": "string",
      "sentAt": "string",
      "serviceGroups": {
        "ungroupedServices": {
          "services": [
            {
              "amount": 1,
              "defaultServiceId": "string",
              "explanation": "string",
              "id": "string",
              "invoiceMethod": "string",
              "name": "Ava Chen",
              "position": 1,
              "price": 1,
              "salesId": "string",
              "showItemtype": true,
              "total": 1,
              "totalInclVat": 1,
              "trackCost": true,
              "trackHours": true,
              "vatCode": "string",
              "vatDescription": "string"
            }
          ],
          "totals": {
            "totalExcluding": {
              "amount": 1,
              "currency": "string"
            },
            "totalIncluding": {
              "amount": 1,
              "currency": "string"
            },
            "totalVat": {
              "amount": 1,
              "currency": "string"
            },
            "vatDivisions": [
              {
                "vatAmount": {
                  "amount": 1,
                  "currency": "string"
                },
                "vatCode": "string",
                "vatDescription": "string"
              }
            ]
          }
        }
      },
      "services": [
        {
          "amount": 1,
          "defaultServiceId": "string",
          "explanation": "string",
          "id": "string",
          "invoiceMethod": "string",
          "name": "Ava Chen",
          "position": 1,
          "price": 1,
          "salesId": "string",
          "showItemtype": true,
          "total": 1,
          "totalInclVat": 1,
          "trackCost": true,
          "trackHours": true,
          "vatCode": "string",
          "vatDescription": "string"
        }
      ],
      "totalExcl": 1,
      "totalIncl": 1,
      "totalVat": 1,
      "updatedAt": "string",
      "validDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.personId` | string |  |
| `customerReference` | string |  |
| `grandTotals.fixed.totalExcluding` | number |  |
| `grandTotals.fixed.totalIncluding` | number |  |
| `grandTotals.fixed.totalVat` | number |  |
| `grandTotals.fixed.vatTypes.21%` | number |  |
| `grandTotals.hours.totalExcluding` | number |  |
| `grandTotals.hours.totalIncluding` | number |  |
| `grandTotals.hours.totalVat` | number |  |
| `grandTotals.hours.vatTypes.21%` | number |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `isOutdated` | boolean |  |
| `isSepaAuthorization` | boolean |  |
| `json` | string |  |
| `lastUpdatedApprovalStatus` | string |  |
| `paymentTerm.days` | string |  |
| `paymentTerm.id` | string |  |
| `paymentTerm.method` | string |  |
| `paymentTerm.name` | string |  |
| `quoteDate` | string |  |
| `quoteNumber` | string |  |
| `quotestatus.color` | string |  |
| `quotestatus.id` | string |  |
| `quotestatus.label` | string |  |
| `quoteSubject` | string |  |
| `quotetemplate.id` | string |  |
| `quotetemplate.name` | string |  |
| `salesId` | string |  |
| `sentAt` | string |  |
| `serviceGroups.ungroupedServices.services[].amount` | number |  |
| `serviceGroups.ungroupedServices.services[].defaultServiceId` | string |  |
| `serviceGroups.ungroupedServices.services[].explanation` | string |  |
| `serviceGroups.ungroupedServices.services[].id` | string |  |
| `serviceGroups.ungroupedServices.services[].invoiceMethod` | string |  |
| `serviceGroups.ungroupedServices.services[].name` | string |  |
| `serviceGroups.ungroupedServices.services[].position` | number |  |
| `serviceGroups.ungroupedServices.services[].price` | number |  |
| `serviceGroups.ungroupedServices.services[].salesId` | string |  |
| `serviceGroups.ungroupedServices.services[].showItemtype` | boolean |  |
| `serviceGroups.ungroupedServices.services[].total` | number |  |
| `serviceGroups.ungroupedServices.services[].totalInclVat` | number |  |
| `serviceGroups.ungroupedServices.services[].trackCost` | boolean |  |
| `serviceGroups.ungroupedServices.services[].trackHours` | boolean |  |
| `serviceGroups.ungroupedServices.services[].vatCode` | string |  |
| `serviceGroups.ungroupedServices.services[].vatDescription` | string |  |
| `serviceGroups.ungroupedServices.totals.totalExcluding.amount` | number |  |
| `serviceGroups.ungroupedServices.totals.totalExcluding.currency` | string |  |
| `serviceGroups.ungroupedServices.totals.totalIncluding.amount` | number |  |
| `serviceGroups.ungroupedServices.totals.totalIncluding.currency` | string |  |
| `serviceGroups.ungroupedServices.totals.totalVat.amount` | number |  |
| `serviceGroups.ungroupedServices.totals.totalVat.currency` | string |  |
| `serviceGroups.ungroupedServices.totals.vatDivisions[].vatAmount.amount` | number |  |
| `serviceGroups.ungroupedServices.totals.vatDivisions[].vatAmount.currency` | string |  |
| `serviceGroups.ungroupedServices.totals.vatDivisions[].vatCode` | string |  |
| `serviceGroups.ungroupedServices.totals.vatDivisions[].vatDescription` | string |  |
| `services[].amount` | number |  |
| `services[].defaultServiceId` | string |  |
| `services[].explanation` | string |  |
| `services[].id` | string |  |
| `services[].invoiceMethod` | string |  |
| `services[].name` | string |  |
| `services[].position` | number |  |
| `services[].price` | number |  |
| `services[].salesId` | string |  |
| `services[].showItemtype` | boolean |  |
| `services[].total` | number |  |
| `services[].totalInclVat` | number |  |
| `services[].trackCost` | boolean |  |
| `services[].trackHours` | boolean |  |
| `services[].vatCode` | string |  |
| `services[].vatDescription` | string |  |
| `totalExcl` | number |  |
| `totalIncl` | number |  |
| `totalVat` | number |  |
| `updatedAt` | string |  |
| `validDays` | number |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /sales/quote` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quote-templates.md) for the provider-specific parameters and requirements.

