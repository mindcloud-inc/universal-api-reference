# OnlineCheckWriter: Get Check

Retrieves details for a specific check.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-check?connectionId=$CONNECTION_ID&checkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-check?${params}`, {
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
| `checkId` | string | yes | The check identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accountNumber": "string",
        "amount": "string",
        "amountInWord": "string",
        "bankAccount": {
          "bankAccountId": "string",
          "name": "Ava Chen"
        },
        "category": {
          "categoryId": "string",
          "name": {}
        },
        "checkId": "string",
        "checkStatus": {
          "description": "string",
          "status": 1
        },
        "date": "2026-05-07T12:00:00.000Z",
        "invoiceNumber": "string",
        "memo": "string",
        "payee": {
          "name": {},
          "payeeId": "string"
        },
        "referenceId": {},
        "serialNumber": "string",
        "status": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accountNumber` | string |  |
| `data.amount` | string |  |
| `data.amountInWord` | string |  |
| `data.bankAccount.bankAccountId` | string |  |
| `data.bankAccount.name` | string |  |
| `data.category.categoryId` | string |  |
| `data.category.name` | object |  |
| `data.checkId` | string |  |
| `data.checkStatus.description` | string |  |
| `data.checkStatus.status` | number |  |
| `data.date` | date |  |
| `data.invoiceNumber` | string |  |
| `data.memo` | string |  |
| `data.payee.name` | object |  |
| `data.payee.payeeId` | string |  |
| `data.referenceId` | object |  |
| `data.serialNumber` | string |  |
| `data.status` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /checks/:checkId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-check.md) for the provider-specific parameters and requirements.

