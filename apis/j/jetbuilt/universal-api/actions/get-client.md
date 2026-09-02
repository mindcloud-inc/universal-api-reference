# Jetbuilt: Get Client

Get a Client

```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-client?${params}`, {
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
| `id` | string | no | Client Id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "city": {},
      "companyName": "Ava Chen",
      "country": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "delinquent": true,
      "id": 1,
      "paymentSchedule": {},
      "primaryContactEmail": {},
      "primaryContactFirstName": {},
      "primaryContactLastName": {},
      "primaryContactPhoneNumber1": {},
      "primaryContactPhoneNumber2": {},
      "primaryContactTitle": {},
      "state": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "zipcode": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `city` | object |  |
| `companyName` | string |  |
| `country` | object |  |
| `createdAt` | date |  |
| `delinquent` | boolean |  |
| `id` | number |  |
| `paymentSchedule` | object |  |
| `primaryContactEmail` | object |  |
| `primaryContactFirstName` | object |  |
| `primaryContactLastName` | object |  |
| `primaryContactPhoneNumber1` | object |  |
| `primaryContactPhoneNumber2` | object |  |
| `primaryContactTitle` | object |  |
| `state` | object |  |
| `updatedAt` | date |  |
| `zipcode` | object |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET clients/:id` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

