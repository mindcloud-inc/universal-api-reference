# Easyship: Get Account Information

Retrieves current account information from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-account-information?${params}`, {
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
      "billingAddress": {
        "city": "string",
        "companyName": "Ava Chen",
        "contactEmail": "ava@example.com",
        "contactName": "Ava Chen",
        "contactPhone": "string",
        "countryAlpha2": "string",
        "defaultFor": {
          "billing": true,
          "pickup": true,
          "return": true,
          "sender": true
        },
        "id": "string",
        "line1": "string",
        "line2": "string",
        "postalCode": "string",
        "state": "string",
        "status": "string"
      },
      "credit": {
        "availableBalance": 1,
        "balance": 1,
        "currency": "string"
      },
      "easyshipCompanyId": "string",
      "name": "Ava Chen",
      "paymentSources": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `billingAddress.city` | string |  |
| `billingAddress.companyName` | string |  |
| `billingAddress.contactEmail` | string |  |
| `billingAddress.contactName` | string |  |
| `billingAddress.contactPhone` | string |  |
| `billingAddress.countryAlpha2` | string |  |
| `billingAddress.defaultFor` | object |  |
| `billingAddress.defaultFor.billing` | boolean |  |
| `billingAddress.defaultFor.pickup` | boolean |  |
| `billingAddress.defaultFor.return` | boolean |  |
| `billingAddress.defaultFor.sender` | boolean |  |
| `billingAddress.id` | string |  |
| `billingAddress.line1` | string |  |
| `billingAddress.line2` | string |  |
| `billingAddress.postalCode` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.status` | string |  |
| `credit` | object |  |
| `credit.availableBalance` | number |  |
| `credit.balance` | number |  |
| `credit.currency` | string |  |
| `easyshipCompanyId` | string |  |
| `name` | string |  |
| `paymentSources` | array<object> |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /account` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

