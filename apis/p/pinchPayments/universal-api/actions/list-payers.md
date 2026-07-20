# Pinch Payments: List Payers

Retrieves payers from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-payers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-payers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-payers?${params}`, {
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
| `filter` | string | no | Optional string filter to search for payers by name or email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "companyName": "Ava Chen",
          "companyRegistrationNumber": "string",
          "country": "string",
          "countryCode": "string",
          "emailAddress": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "metadata": "string",
          "mobileNumber": "string",
          "postcode": "string",
          "state": "string",
          "streetAddress": "string",
          "suburb": "string"
        }
      ],
      "page": 1,
      "pageSize": 1,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].companyName` | string |  |
| `data[].companyRegistrationNumber` | string |  |
| `data[].country` | string |  |
| `data[].countryCode` | string |  |
| `data[].emailAddress` | string |  |
| `data[].firstName` | string |  |
| `data[].id` | string |  |
| `data[].lastName` | string |  |
| `data[].metadata` | string |  |
| `data[].mobileNumber` | string |  |
| `data[].postcode` | string |  |
| `data[].state` | string |  |
| `data[].streetAddress` | string |  |
| `data[].suburb` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `totalItems` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /payers` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payers.md) for the provider-specific parameters and requirements.

