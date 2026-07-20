# Lodgify: List Properties

Retrieves a list of properties from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-properties?${params}`, {
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
      "address": "string",
      "city": "string",
      "contact": {},
      "country": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "description": "string",
      "hasAddons": true,
      "hasAgreement": true,
      "hideAddress": true,
      "id": 1,
      "imageUrl": "https://example.com",
      "inOutMaxDate": "2026-05-07T12:00:00.000Z",
      "internalName": "Ava Chen",
      "isActive": true,
      "latitude": 1,
      "longitude": 1,
      "maxPrice": 1,
      "minPrice": 1,
      "name": "Ava Chen",
      "originalMaxPrice": 1,
      "originalMinPrice": 1,
      "priceUnitInDays": 1,
      "rating": 1,
      "rooms": [
        {}
      ],
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `contact` | object |  |
| `country` | string |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `hasAddons` | boolean |  |
| `hasAgreement` | boolean |  |
| `hideAddress` | boolean |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `inOutMaxDate` | date |  |
| `internalName` | string |  |
| `isActive` | boolean |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `maxPrice` | number |  |
| `minPrice` | number |  |
| `name` | string |  |
| `originalMaxPrice` | number |  |
| `originalMinPrice` | number |  |
| `priceUnitInDays` | number |  |
| `rating` | number |  |
| `rooms` | array<object> |  |
| `state` | string |  |
| `updatedAt` | date |  |
| `zip` | string |  |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v2/properties` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

