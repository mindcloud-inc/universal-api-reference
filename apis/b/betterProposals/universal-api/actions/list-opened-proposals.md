# Better Proposals: List Opened Proposals

Retrieves opened proposals from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-opened-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-opened-proposals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-opened-proposals?${params}`, {
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
| `page` | number | no | Page number. Default: 1. Default: `1`. |
| `perPage` | number | no | Results per page. Default: 10. Default: `10`. |
| `documentTypeId` | string | no | DocumentTypeID for filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annualTotal": "string",
      "brandID": "string",
      "companyCRMID": {},
      "companyName": "Ava Chen",
      "contacts": [
        {
          "email": "ava@example.com",
          "firstName": "Ava",
          "link": "https://example.com",
          "surname": "Ava Chen"
        }
      ],
      "coverID": "string",
      "cRMOpportunityID": {},
      "currencyCode": "string",
      "currencyName": "Ava Chen",
      "currencySymbol": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": {},
      "emailMessage": "ava@example.com",
      "id": "string",
      "lastDateSent": "2026-05-07T12:00:00.000Z",
      "monthlyTotal": "string",
      "oneOffTotal": "string",
      "originalDateSent": "2026-05-07T12:00:00.000Z",
      "preview": "string",
      "priceTables": [
        {
          "dateCreated": "2026-05-07T12:00:00.000Z",
          "displayOrder": 1,
          "forceClientChoice": true,
          "id": "string",
          "items": [
            {
              "canClientSetQuantity": true,
              "cost": "string",
              "date": {},
              "description": "string",
              "discount": true,
              "discountAmount": "string",
              "discountType": true,
              "displayOrder": 1,
              "id": "string",
              "isQuantityLimited": true,
              "label": "string",
              "monthlyCost": "string",
              "optional": true,
              "priceType": "string",
              "quantity": 1,
              "quantityMax": 1,
              "quantityMin": 1,
              "recurringType": "string",
              "selectable": true,
              "selected": true,
              "showQuantity": true,
              "tableDiscount": true,
              "tableDiscountAmount": "string",
              "tableDiscountType": true,
              "taxExemptionStatus": true,
              "unitCost": "string"
            }
          ],
          "show": true,
          "title": "string"
        }
      ],
      "proposalOpened": "string",
      "proposalView": "string",
      "quarterlyTotal": "string",
      "quoteID": "string",
      "subjectLine": "string",
      "taxName": "Ava Chen",
      "taxPercentage": "string",
      "typeID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annualTotal` | string |  |
| `brandID` | string |  |
| `companyCRMID` | object |  |
| `companyName` | string |  |
| `contacts[].email` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].link` | string |  |
| `contacts[].surname` | string |  |
| `coverID` | string |  |
| `cRMOpportunityID` | object |  |
| `currencyCode` | string |  |
| `currencyName` | string |  |
| `currencySymbol` | string |  |
| `dateCreated` | date |  |
| `description` | object |  |
| `emailMessage` | string |  |
| `id` | string |  |
| `lastDateSent` | date |  |
| `monthlyTotal` | string |  |
| `oneOffTotal` | string |  |
| `originalDateSent` | date |  |
| `preview` | string |  |
| `priceTables[].dateCreated` | date |  |
| `priceTables[].displayOrder` | number |  |
| `priceTables[].forceClientChoice` | boolean |  |
| `priceTables[].id` | string |  |
| `priceTables[].items[].canClientSetQuantity` | boolean |  |
| `priceTables[].items[].cost` | string |  |
| `priceTables[].items[].date` | object |  |
| `priceTables[].items[].description` | string |  |
| `priceTables[].items[].discount` | boolean |  |
| `priceTables[].items[].discountAmount` | string |  |
| `priceTables[].items[].discountType` | boolean |  |
| `priceTables[].items[].displayOrder` | number |  |
| `priceTables[].items[].id` | string |  |
| `priceTables[].items[].isQuantityLimited` | boolean |  |
| `priceTables[].items[].label` | string |  |
| `priceTables[].items[].monthlyCost` | string |  |
| `priceTables[].items[].optional` | boolean |  |
| `priceTables[].items[].priceType` | string |  |
| `priceTables[].items[].quantity` | number |  |
| `priceTables[].items[].quantityMax` | number |  |
| `priceTables[].items[].quantityMin` | number |  |
| `priceTables[].items[].recurringType` | string |  |
| `priceTables[].items[].selectable` | boolean |  |
| `priceTables[].items[].selected` | boolean |  |
| `priceTables[].items[].showQuantity` | boolean |  |
| `priceTables[].items[].tableDiscount` | boolean |  |
| `priceTables[].items[].tableDiscountAmount` | string |  |
| `priceTables[].items[].tableDiscountType` | boolean |  |
| `priceTables[].items[].taxExemptionStatus` | boolean |  |
| `priceTables[].items[].unitCost` | string |  |
| `priceTables[].show` | boolean |  |
| `priceTables[].title` | string |  |
| `proposalOpened` | string |  |
| `proposalView` | string |  |
| `quarterlyTotal` | string |  |
| `quoteID` | string |  |
| `subjectLine` | string |  |
| `taxName` | string |  |
| `taxPercentage` | string |  |
| `typeID` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /proposal/opened` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opened-proposals.md) for the provider-specific parameters and requirements.

