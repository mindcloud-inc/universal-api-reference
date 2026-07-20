# Teletype App: Get Project Tariff

Retrieves project tariff from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-tariff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-tariff?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-tariff?${params}`, {
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
      "active": true,
      "autopayAmount": 1,
      "autopayBalance": 1,
      "autopayEnabled": true,
      "balance": {},
      "dailyPayment": 1,
      "dailyPaymentByPrice": 1,
      "options": {},
      "packagePrice": [
        {}
      ],
      "packages": [
        {}
      ],
      "paid": true,
      "project": {},
      "promoDaysGranted": 1,
      "promoDaysRemain": 1,
      "promoEndDate": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `autopayAmount` | number |  |
| `autopayBalance` | number |  |
| `autopayEnabled` | boolean |  |
| `balance` | object |  |
| `dailyPayment` | number |  |
| `dailyPaymentByPrice` | number |  |
| `options` | object |  |
| `packagePrice` | array<object> |  |
| `packages` | array<object> |  |
| `paid` | boolean |  |
| `project` | object |  |
| `promoDaysGranted` | number |  |
| `promoDaysRemain` | number |  |
| `promoEndDate` | object |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /project/tariff` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-tariff.md) for the provider-specific parameters and requirements.

