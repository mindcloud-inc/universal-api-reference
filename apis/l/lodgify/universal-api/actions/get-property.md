# Lodgify: Get Property

Retrieves details for a property from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-property?connectionId=$CONNECTION_ID&id=779887" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "779887"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-property?${params}`, {
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
| `id` | number | yes | The Lodgify property ID Example: `779887`. |

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
| `address` | string | Street address. |
| `city` | string | City. |
| `contact` | object | Contact details. |
| `country` | string | Country name. |
| `countryCode` | string | Country code. |
| `createdAt` | date | Created timestamp. |
| `currencyCode` | string | Currency code. |
| `description` | string | Property description. |
| `hasAddons` | boolean | Whether addons are enabled. |
| `hasAgreement` | boolean | Whether an agreement is required. |
| `hideAddress` | boolean | Whether the address is hidden. |
| `id` | number | Property ID. |
| `imageUrl` | string | Primary property image URL. |
| `inOutMaxDate` | date | Maximum in/out date. |
| `internalName` | string | Internal property name. |
| `isActive` | boolean | Whether the property is active. |
| `latitude` | number | Latitude. |
| `longitude` | number | Longitude. |
| `maxPrice` | number | Maximum price. |
| `minPrice` | number | Minimum price. |
| `name` | string | Property name. |
| `originalMaxPrice` | number | Original maximum price before discounts. |
| `originalMinPrice` | number | Original minimum price before discounts. |
| `priceUnitInDays` | number | Pricing unit duration in days. |
| `rating` | number | Property rating. |
| `rooms` | array<object> | Room list. |
| `state` | string | State or region. |
| `updatedAt` | date | Updated timestamp. |
| `zip` | string | Postal code. |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v2/properties/:id` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property.md) for the provider-specific parameters and requirements.

