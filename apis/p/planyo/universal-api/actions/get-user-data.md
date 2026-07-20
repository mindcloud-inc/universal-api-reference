# Planyo: Get User Data

Retrieves user data from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-user-data?${params}`, {
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
| `userId` | number | no |  |
| `email` | string | no |  |
| `siteId` | number | no |  |
| `detailLevel` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "ipAddress": "string",
      "isEmailVerified": true,
      "language": "string",
      "lastName": "Chen",
      "lastReservation": "string",
      "login": "string",
      "mobileNumber": "string",
      "phoneNumber": "string",
      "registrationTime": "string",
      "reservationCount": 1,
      "state": "string",
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
| `country` | string |  |
| `countryCode` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `ipAddress` | string |  |
| `isEmailVerified` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `lastReservation` | string |  |
| `login` | string |  |
| `mobileNumber` | string |  |
| `phoneNumber` | string |  |
| `registrationTime` | string |  |
| `reservationCount` | number |  |
| `state` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-data.md) for the provider-specific parameters and requirements.

