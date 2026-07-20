# OnlineCheckWriter: Get Bank Account

Retrieves details for a specific bank account.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-bank-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-bank-account?connectionId=$CONNECTION_ID&bankAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bankAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-bank-account?${params}`, {
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
| `bankAccountId` | string | yes | The bank account identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accountNumber": "string",
        "addressLine1": {},
        "addressLine2": {},
        "bankAccountId": "string",
        "bankId": "string",
        "city": {},
        "createdDate": "string",
        "id": "string",
        "isAchEnabled": true,
        "isVerified": true,
        "name": "Ava Chen",
        "nickName": "Ava Chen",
        "phone": {},
        "routingNumber": "string",
        "state": {},
        "webUrl": "https://example.com",
        "zip": {}
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
| `data.addressLine1` | object |  |
| `data.addressLine2` | object |  |
| `data.bankAccountId` | string |  |
| `data.bankId` | string |  |
| `data.city` | object |  |
| `data.createdDate` | string |  |
| `data.id` | string |  |
| `data.isAchEnabled` | boolean |  |
| `data.isVerified` | boolean |  |
| `data.name` | string |  |
| `data.nickName` | string |  |
| `data.phone` | object |  |
| `data.routingNumber` | string |  |
| `data.state` | object |  |
| `data.webUrl` | string |  |
| `data.zip` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /bankAccounts/:bankAccountId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bank-account.md) for the provider-specific parameters and requirements.

