# Invoice Ninja: List Quotes



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-quotes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-quotes?${params}`, {
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
| `status` | string | no | Optional status filter such as active, archived, or deleted. |
| `clientId` | string | no | Optional client filter using the hashed client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archivedAt": 1,
      "assignedUserId": "string",
      "balance": 1,
      "clientId": "string",
      "createdAt": 1,
      "customSurcharge1": 1,
      "customSurcharge2": 1,
      "customSurcharge3": 1,
      "customSurcharge4": 1,
      "customSurchargeTax1": true,
      "customSurchargeTax2": true,
      "customSurchargeTax3": true,
      "customSurchargeTax4": true,
      "customValue1": "string",
      "customValue2": "string",
      "customValue3": "string",
      "customValue4": "string",
      "date": "string",
      "designId": "string",
      "discount": 1,
      "dueDate": "string",
      "entityType": "string",
      "exchangeRate": 1,
      "footer": "string",
      "hasExpenses": true,
      "hasTasks": true,
      "id": "string",
      "invitations": [
        {
          "archivedAt": 1,
          "canSign": true,
          "clientContactId": "string",
          "createdAt": 1,
          "emailError": "ava@example.com",
          "emailStatus": "ava@example.com",
          "id": "string",
          "key": "string",
          "link": "https://example.com",
          "messageId": "string",
          "openedDate": "string",
          "sentDate": "string",
          "updatedAt": 1,
          "viewedDate": "string"
        }
      ],
      "invoiceId": "string",
      "isAmountDiscount": true,
      "isDeleted": true,
      "lastSentDate": "string",
      "lineItems": [
        {
          "cost": 1,
          "customValue1": "string",
          "customValue2": "string",
          "customValue3": "string",
          "customValue4": "string",
          "date": "string",
          "discount": 1,
          "expenseId": "string",
          "grossLineTotal": 1,
          "incomeAccountId": "string",
          "isAmountDiscount": true,
          "lineTotal": 1,
          "netCost": 1,
          "notes": "string",
          "productCost": 1,
          "productKey": "string",
          "quantity": 1,
          "sortId": "string",
          "taskId": "string",
          "taxAmount": 1,
          "taxId": "string",
          "taxName1": "Ava Chen",
          "taxName2": "Ava Chen",
          "taxName3": "Ava Chen",
          "taxRate1": 1,
          "taxRate2": 1,
          "taxRate3": 1,
          "typeId": "string",
          "unitCode": "string"
        }
      ],
      "locationId": "string",
      "nextSendDate": "string",
      "number": "string",
      "paidToDate": 1,
      "partial": 1,
      "partialDueDate": "string",
      "poNumber": "string",
      "privateNotes": "string",
      "projectId": "string",
      "publicNotes": "string",
      "reminder1Sent": "string",
      "reminder2Sent": "string",
      "reminder3Sent": "string",
      "reminderLastSent": "string",
      "statusId": "string",
      "subscriptionId": "string",
      "sync": {},
      "taxName1": "Ava Chen",
      "taxName2": "Ava Chen",
      "taxName3": "Ava Chen",
      "taxRate1": 1,
      "taxRate2": 1,
      "taxRate3": 1,
      "terms": "string",
      "totalTaxes": 1,
      "updatedAt": 1,
      "userId": "string",
      "usesInclusiveTaxes": true,
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `archivedAt` | number |  |
| `assignedUserId` | string |  |
| `balance` | number |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `customSurcharge1` | number |  |
| `customSurcharge2` | number |  |
| `customSurcharge3` | number |  |
| `customSurcharge4` | number |  |
| `customSurchargeTax1` | boolean |  |
| `customSurchargeTax2` | boolean |  |
| `customSurchargeTax3` | boolean |  |
| `customSurchargeTax4` | boolean |  |
| `customValue1` | string |  |
| `customValue2` | string |  |
| `customValue3` | string |  |
| `customValue4` | string |  |
| `date` | string |  |
| `designId` | string |  |
| `discount` | number |  |
| `dueDate` | string |  |
| `entityType` | string |  |
| `exchangeRate` | number |  |
| `footer` | string |  |
| `hasExpenses` | boolean |  |
| `hasTasks` | boolean |  |
| `id` | string |  |
| `invitations[].archivedAt` | number |  |
| `invitations[].canSign` | boolean |  |
| `invitations[].clientContactId` | string |  |
| `invitations[].createdAt` | number |  |
| `invitations[].emailError` | string |  |
| `invitations[].emailStatus` | string |  |
| `invitations[].id` | string |  |
| `invitations[].key` | string |  |
| `invitations[].link` | string |  |
| `invitations[].messageId` | string |  |
| `invitations[].openedDate` | string |  |
| `invitations[].sentDate` | string |  |
| `invitations[].updatedAt` | number |  |
| `invitations[].viewedDate` | string |  |
| `invoiceId` | string |  |
| `isAmountDiscount` | boolean |  |
| `isDeleted` | boolean |  |
| `lastSentDate` | string |  |
| `lineItems[].cost` | number |  |
| `lineItems[].customValue1` | string |  |
| `lineItems[].customValue2` | string |  |
| `lineItems[].customValue3` | string |  |
| `lineItems[].customValue4` | string |  |
| `lineItems[].date` | string |  |
| `lineItems[].discount` | number |  |
| `lineItems[].expenseId` | string |  |
| `lineItems[].grossLineTotal` | number |  |
| `lineItems[].incomeAccountId` | string |  |
| `lineItems[].isAmountDiscount` | boolean |  |
| `lineItems[].lineTotal` | number |  |
| `lineItems[].netCost` | number |  |
| `lineItems[].notes` | string |  |
| `lineItems[].productCost` | number |  |
| `lineItems[].productKey` | string |  |
| `lineItems[].quantity` | number |  |
| `lineItems[].sortId` | string |  |
| `lineItems[].taskId` | string |  |
| `lineItems[].taxAmount` | number |  |
| `lineItems[].taxId` | string |  |
| `lineItems[].taxName1` | string |  |
| `lineItems[].taxName2` | string |  |
| `lineItems[].taxName3` | string |  |
| `lineItems[].taxRate1` | number |  |
| `lineItems[].taxRate2` | number |  |
| `lineItems[].taxRate3` | number |  |
| `lineItems[].typeId` | string |  |
| `lineItems[].unitCode` | string |  |
| `locationId` | string |  |
| `nextSendDate` | string |  |
| `number` | string |  |
| `paidToDate` | number |  |
| `partial` | number |  |
| `partialDueDate` | string |  |
| `poNumber` | string |  |
| `privateNotes` | string |  |
| `projectId` | string |  |
| `publicNotes` | string |  |
| `reminder1Sent` | string |  |
| `reminder2Sent` | string |  |
| `reminder3Sent` | string |  |
| `reminderLastSent` | string |  |
| `statusId` | string |  |
| `subscriptionId` | string |  |
| `sync` | object |  |
| `taxName1` | string |  |
| `taxName2` | string |  |
| `taxName3` | string |  |
| `taxRate1` | number |  |
| `taxRate2` | number |  |
| `taxRate3` | number |  |
| `terms` | string |  |
| `totalTaxes` | number |  |
| `updatedAt` | number |  |
| `userId` | string |  |
| `usesInclusiveTaxes` | boolean |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /quotes` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

