# Bokun: Get Customer

Retrieves a customer by ID from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | The Bokun customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "language": "string",
      "lastName": "Chen",
      "nationality": "string",
      "organization": "string",
      "passportId": "string",
      "phoneNumber": "string",
      "postCode": "string",
      "sex": "string",
      "state": "string",
      "title": "string"
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
| `dateOfBirth` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `language` | string |  |
| `lastName` | string |  |
| `nationality` | string |  |
| `organization` | string |  |
| `passportId` | string |  |
| `phoneNumber` | string |  |
| `postCode` | string |  |
| `sex` | string |  |
| `state` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/customer/:customerId` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

