# Fidel API: Update Location

Updates an existing location in Fidel API.

```
PUT https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": "string",
  "address": "string",
  "city": "string",
  "countryCode": "string",
  "postcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": "string",
    "address": "string",
    "city": "string",
    "countryCode": "string",
    "postcode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | string | yes |  |
| `address` | string | yes | Address for the location. |
| `city` | string | yes | City for the location. |
| `countryCode` | string | yes | ISO alpha-3 country code for the location. |
| `postcode` | string | yes | Postcode for the location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "active": true,
      "activeDate": "2026-05-07T12:00:00.000Z",
      "address": "string",
      "amex": {
        "auth": true,
        "clearing": true,
        "status": "string"
      },
      "brandId": "string",
      "city": "string",
      "countryCode": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "geolocation": {
        "latitude": 1,
        "longitude": 1
      },
      "id": "string",
      "live": true,
      "mastercard": {
        "auth": true,
        "clearing": true,
        "status": "string"
      },
      "postcode": "string",
      "preonboard": true,
      "programId": "string",
      "timezone": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visa": {
        "auth": true,
        "clearing": true,
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `active` | boolean |  |
| `activeDate` | date |  |
| `address` | string |  |
| `amex.auth` | boolean |  |
| `amex.clearing` | boolean |  |
| `amex.status` | string |  |
| `brandId` | string |  |
| `city` | string |  |
| `countryCode` | string |  |
| `created` | date |  |
| `currency` | string |  |
| `geolocation.latitude` | number |  |
| `geolocation.longitude` | number |  |
| `id` | string |  |
| `live` | boolean |  |
| `mastercard.auth` | boolean |  |
| `mastercard.clearing` | boolean |  |
| `mastercard.status` | string |  |
| `postcode` | string |  |
| `preonboard` | boolean |  |
| `programId` | string |  |
| `timezone` | string |  |
| `updated` | date |  |
| `visa.auth` | boolean |  |
| `visa.clearing` | boolean |  |
| `visa.status` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `PATCH /locations/:locationId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

