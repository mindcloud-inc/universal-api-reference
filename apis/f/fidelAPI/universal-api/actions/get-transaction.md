# Fidel API: Get Transaction

Retrieves a transaction from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-transaction?${params}`, {
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
| `transactionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "amount": 1,
      "auth": true,
      "authCode": "string",
      "brand": {
        "id": "string",
        "name": "Ava Chen"
      },
      "card": {
        "firstNumbers": "string",
        "id": "string",
        "lastNumbers": "string",
        "scheme": "string"
      },
      "cleared": true,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "identifiers": {
        "MID": "string",
        "visaAuthCode": "string"
      },
      "location": {
        "address": "string",
        "city": "string",
        "countryCode": "string",
        "geolocation": {
          "latitude": 1,
          "longitude": 1
        },
        "id": "string",
        "postcode": "string",
        "timezone": "string"
      },
      "programId": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `amount` | number |  |
| `auth` | boolean |  |
| `authCode` | string |  |
| `brand.id` | string |  |
| `brand.name` | string |  |
| `card.firstNumbers` | string |  |
| `card.id` | string |  |
| `card.lastNumbers` | string |  |
| `card.scheme` | string |  |
| `cleared` | boolean |  |
| `created` | date |  |
| `currency` | string |  |
| `datetime` | date |  |
| `id` | string |  |
| `identifiers.MID` | string |  |
| `identifiers.visaAuthCode` | string |  |
| `location.address` | string |  |
| `location.city` | string |  |
| `location.countryCode` | string |  |
| `location.geolocation.latitude` | number |  |
| `location.geolocation.longitude` | number |  |
| `location.id` | string |  |
| `location.postcode` | string |  |
| `location.timezone` | string |  |
| `programId` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /transactions/:transactionId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

