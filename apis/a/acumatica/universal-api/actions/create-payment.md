# Acumatica: Create Payment



```
POST https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId.value": "FRUITICO",
  "cashAccount.value": "10250ST",
  "paymentAmount.value": "235.27",
  "paymentMethod.value": "CHECK"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId.value": "FRUITICO",
    "cashAccount.value": "10250ST",
    "paymentAmount.value": "235.27",
    "paymentMethod.value": "CHECK"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | object | no |  |
| `customerId.value` | string | yes | Example: `FRUITICO`. |
| `cashAccount` | object | no |  |
| `cashAccount.value` | string | yes | Example: `10250ST`. |
| `paymentAmount` | object | no |  |
| `paymentAmount.value` | number | yes | Example: `235.27`. |
| `paymentMethod` | object | no |  |
| `paymentMethod.value` | string | yes | Example: `CHECK`. |
| `hold` | object | no |  |
| `hold.value` | boolean | no | Example: `false`. |
| `description` | object | no |  |
| `description.value` | string | no | Example: `Customer payment`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch` | object | no |  |
| `branch.value` | string | no | Example: `HEADOFFICE`. |
| `currencyId` | object | no |  |
| `currencyId.value` | string | no | Example: `USD`. |
| `documentsToApply[]` | array<object> | no |  |
| `documentsToApply[].docType` | object | no |  |
| `documentsToApply[].docType.value` | string | no | Example: `INV`. |
| `documentsToApply[].docLineNbr` | object | no |  |
| `documentsToApply[].docLineNbr.value` | string | no | Example: `1`. |
| `documentsToApply[].referenceNbr` | object | no |  |
| `documentsToApply[].referenceNbr.value` | string | no | Example: `000002`. |
| `ordersToApply[]` | array<object> | no |  |
| `ordersToApply[].orderType` | object | no |  |
| `ordersToApply[].orderType.value` | string | no | Example: `SO`. |
| `ordersToApply[].orderNbr` | object | no |  |
| `ordersToApply[].orderNbr.value` | string | no | Example: `000036`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "ApplicationDate": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "AppliedToDocuments": {
        "value": 1
      },
      "Branch": {
        "value": "string"
      },
      "CashAccount": {
        "value": "string"
      },
      "CurrencyID": {
        "value": "string"
      },
      "CustomerID": {
        "value": "string"
      },
      "Description": {
        "value": "string"
      },
      "Hold": {
        "value": true
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "note": {
        "value": "string"
      },
      "PaymentAmount": {
        "value": 1
      },
      "PaymentMethod": {
        "value": "string"
      },
      "PaymentRef": {
        "value": "string"
      },
      "ReferenceNbr": {
        "value": "string"
      },
      "rowNumber": 1,
      "SaveCard": {
        "value": true
      },
      "Status": {
        "value": "string"
      },
      "Type": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.files:put` | string |  |
| `_links.self` | string |  |
| `ApplicationDate.value` | date |  |
| `AppliedToDocuments.value` | number |  |
| `Branch.value` | string |  |
| `CashAccount.value` | string |  |
| `CurrencyID.value` | string |  |
| `CustomerID.value` | string |  |
| `Description.value` | string |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | date |  |
| `note.value` | string |  |
| `PaymentAmount.value` | number |  |
| `PaymentMethod.value` | string |  |
| `PaymentRef.value` | string |  |
| `ReferenceNbr.value` | string |  |
| `rowNumber` | number |  |
| `SaveCard.value` | boolean |  |
| `Status.value` | string |  |
| `Type.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

