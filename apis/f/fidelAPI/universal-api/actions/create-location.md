# Fidel API: Create Location

Creates a location in a Fidel program.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string",
  "address": "string",
  "brandId": "string",
  "city": "string",
  "countryCode": "string",
  "postcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "programId": "string",
    "address": "string",
    "brandId": "string",
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
| `programId` | string | yes |  |
| `address` | string | yes | 2 - 100 characters. |
| `brandId` | string | yes | Brand identifier for the location. |
| `city` | string | yes | 2 - 100 characters. |
| `countryCode` | string | yes | Allowed values: CAN, DNK, FIN, GBR, IRL, JPN, NOR, SWE, USA. |
| `postcode` | string | yes | 4 - 20 characters. |

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

Through the native Fidel API API, this operation is `POST /programs/:programId/locations` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

