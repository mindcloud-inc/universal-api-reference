# Fidel API: List Transactions by Program

Retrieves transactions for a Fidel program.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-transactions-by-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-transactions-by-program?connectionId=$CONNECTION_ID&limit=25&offset=0&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-transactions-by-program?${params}`, {
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
| `programId` | string | yes |  |

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

Through the native Fidel API API, this operation is `GET /programs/:programId/transactions` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions-by-program.md) for the provider-specific parameters and requirements.

