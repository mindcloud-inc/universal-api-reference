# Easyship: List Couriers

Retrieves a list of couriers from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-couriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-couriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-couriers?${params}`, {
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
      "auth": {
        "errors": [
          {}
        ],
        "state": "string"
      },
      "easyshipCourier": true,
      "filteredAccountDetails": {
        "accountNumber": "string",
        "apiKey": "string",
        "siteId": "string"
      },
      "id": "string",
      "logoUrl": "https://example.com",
      "originCountryAlpha2": "string",
      "umbrellaName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | object |  |
| `auth.errors` | array<object> |  |
| `auth.state` | string |  |
| `easyshipCourier` | boolean |  |
| `filteredAccountDetails` | object |  |
| `filteredAccountDetails.accountNumber` | string |  |
| `filteredAccountDetails.apiKey` | string |  |
| `filteredAccountDetails.siteId` | string |  |
| `id` | string |  |
| `logoUrl` | string |  |
| `originCountryAlpha2` | string |  |
| `umbrellaName` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /couriers` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-couriers.md) for the provider-specific parameters and requirements.

