# Pinch Payments: Get Payer

Retrieves a payer from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-payer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-payer?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-payer?${params}`, {
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
| `id` | string | yes | Payer ID in pyr_XXXXXXXXXXXXX format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreements": [
        {}
      ],
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
      "sources": [
        {}
      ],
      "state": "string",
      "streetAddress": "string",
      "suburb": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreements` | array<object> |  |
| `companyName` | string |  |
| `companyRegistrationNumber` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `emailAddress` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `metadata` | string |  |
| `mobileNumber` | string |  |
| `postcode` | string |  |
| `sources` | array<object> |  |
| `state` | string |  |
| `streetAddress` | string |  |
| `suburb` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /payers/[:id]` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payer.md) for the provider-specific parameters and requirements.

