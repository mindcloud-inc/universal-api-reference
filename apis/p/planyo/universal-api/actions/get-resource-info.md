# Planyo: Get Resource Info

Retrieves resource information from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-resource-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-resource-info?connectionId=$CONNECTION_ID&resourceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-resource-info?${params}`, {
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
| `resourceId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "confirmationType": "string",
      "currency": "string",
      "endHour": "string",
      "eventDates": [
        "string"
      ],
      "isListed": "string",
      "isOvernightStay": "string",
      "isPublished": "string",
      "maxDaysToRental": "string",
      "maxQuantityPerRental": "string",
      "maxRentalTime": "string",
      "minHoursToRental": "string",
      "minRentalTime": "string",
      "minTimeBetweenRentals": 1,
      "name": "Ava Chen",
      "photos": [
        {}
      ],
      "prepaymentAmount": "string",
      "prepaymentAmountValidUntil": 1,
      "priceType": "string",
      "properties": {},
      "quantity": "string",
      "resourceAdminEmail": "ava@example.com",
      "resourceAdminId": "string",
      "resourceAdminName": "Ava Chen",
      "sharingMode": "string",
      "siteId": "string",
      "startHour": "string",
      "startQuarters": "string",
      "startTimes": [
        "string"
      ],
      "timeUnit": 1,
      "translatedName": "Ava Chen",
      "unitPrice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `confirmationType` | string |  |
| `currency` | string |  |
| `endHour` | string |  |
| `eventDates` | array<string> |  |
| `isListed` | string |  |
| `isOvernightStay` | string |  |
| `isPublished` | string |  |
| `maxDaysToRental` | string |  |
| `maxQuantityPerRental` | string |  |
| `maxRentalTime` | string |  |
| `minHoursToRental` | string |  |
| `minRentalTime` | string |  |
| `minTimeBetweenRentals` | number |  |
| `name` | string |  |
| `photos` | array<object> |  |
| `prepaymentAmount` | string |  |
| `prepaymentAmountValidUntil` | number |  |
| `priceType` | string |  |
| `properties` | object |  |
| `quantity` | string |  |
| `resourceAdminEmail` | string |  |
| `resourceAdminId` | string |  |
| `resourceAdminName` | string |  |
| `sharingMode` | string |  |
| `siteId` | string |  |
| `startHour` | string |  |
| `startQuarters` | string |  |
| `startTimes` | array<string> |  |
| `timeUnit` | number |  |
| `translatedName` | string |  |
| `unitPrice` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-info.md) for the provider-specific parameters and requirements.

