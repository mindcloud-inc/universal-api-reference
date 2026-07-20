# Easyship: List Courier Services

Retrieves a list of courier services from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-courier-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-courier-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-courier-services?${params}`, {
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
      "accepts": {
        "documents": true,
        "liquids": true,
        "outbounds": true,
        "parcels": true,
        "payOnScanReturns": true,
        "pi965Batteries": true,
        "pi966Batteries": true,
        "pi967Batteries": true,
        "prepaidReturns": true,
        "specificDangerousGoods": true
      },
      "acceptsOutbounds": true,
      "acceptsPayOnScanReturns": true,
      "acceptsPrepaidReturns": true,
      "active": true,
      "availableHandoverOptions": [
        "string"
      ],
      "countryAlpha2": "string",
      "courierId": "string",
      "courierLogoUrl": "https://example.com",
      "domestic": true,
      "easyshipCourierService": true,
      "id": "string",
      "international": true,
      "iossSupport": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "officialName": "Ava Chen",
      "restrictedToDestinationStates": [
        "string"
      ],
      "restrictedToOriginStates": [
        "string"
      ],
      "serviceName": "Ava Chen",
      "supportedIncoterms": [
        "string"
      ],
      "trackingRating": 1,
      "umbrellaName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepts` | object |  |
| `accepts.documents` | boolean |  |
| `accepts.liquids` | boolean |  |
| `accepts.outbounds` | boolean |  |
| `accepts.parcels` | boolean |  |
| `accepts.payOnScanReturns` | boolean |  |
| `accepts.pi965Batteries` | boolean |  |
| `accepts.pi966Batteries` | boolean |  |
| `accepts.pi967Batteries` | boolean |  |
| `accepts.prepaidReturns` | boolean |  |
| `accepts.specificDangerousGoods` | boolean |  |
| `acceptsOutbounds` | boolean |  |
| `acceptsPayOnScanReturns` | boolean |  |
| `acceptsPrepaidReturns` | boolean |  |
| `active` | boolean |  |
| `availableHandoverOptions` | array<string> |  |
| `countryAlpha2` | string |  |
| `courierId` | string |  |
| `courierLogoUrl` | string |  |
| `domestic` | boolean |  |
| `easyshipCourierService` | boolean |  |
| `id` | string |  |
| `international` | boolean |  |
| `iossSupport` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `nickname` | string |  |
| `officialName` | string |  |
| `restrictedToDestinationStates` | array<string> |  |
| `restrictedToOriginStates` | array<string> |  |
| `serviceName` | string |  |
| `supportedIncoterms` | array<string> |  |
| `trackingRating` | number |  |
| `umbrellaName` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /courier_services` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courier-services.md) for the provider-specific parameters and requirements.

