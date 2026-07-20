# Pinch Payments: Create or Update Payer

Creates or updates a payer in Pinch Payments.

```
POST https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "ava@example.com",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "ava@example.com",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | no | Company name for the payer. |
| `companyRegistrationNumber` | string | no | Company registration number for the payer. |
| `country` | string | no | Country for the payer. |
| `emailAddress` | string | yes | Email address for the payer. |
| `firstName` | string | yes | First name for the payer. |
| `fullName` | string | no | Full name for the payer. |
| `id` | string | no | If you include an ID this endpoint updates an existing payer; otherwise it creates a new payer. |
| `lastName` | string | no | Last name for the payer. |
| `metadata` | string | no | Additional metadata for the payer. |
| `mobileNumber` | string | no | Mobile number for the payer. |
| `postcode` | string | no | Postcode for the payer. |
| `source.ipAddress` | string | no | IP address associated with the payment source. |
| `source.sourceType` | string | no | Currently either bank-account or credit-card when creating a payment source with the payer. |
| `source.token` | string | no | Token created by the capture script when adding a payment source with the payer. |
| `state` | string | no | State for the payer. |
| `streetAddress` | string | no | Street address for the payer. |
| `suburb` | string | no | Suburb for the payer. |

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

Through the native Pinch Payments API, this operation is `POST /payers` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-payer.md) for the provider-specific parameters and requirements.

