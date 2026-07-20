# HirePOS: Create Customer

Creates a new customer in HirePOS.

```
POST https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressLine1` | string | no | Primary customer address line. |
| `addressLine2` | string | no | Secondary customer address line. |
| `city` | string | no | Customer city. |
| `company` | string | no | Customer company name. |
| `country` | string | no | Customer country. |
| `email` | string | no | Customer email address. |
| `fax` | string | no | Customer fax number. |
| `firstName` | string | no | Customer first name. |
| `isMobile1` | boolean | no | Whether Phone 1 is a mobile number. |
| `isMobile2` | boolean | no | Whether Phone 2 is a mobile number. |
| `isMobile3` | boolean | no | Whether Phone 3 is a mobile number. |
| `lastName` | string | no | Customer last name. |
| `notes` | string | no | Additional customer notes. |
| `phone1` | string | no | Primary customer phone number. |
| `phone2` | string | no | Secondary customer phone number. |
| `phone3` | string | no | Third customer phone number. |
| `postcode` | string | no | Customer postcode. |
| `referralSource` | string | no | How the customer found the business. |
| `state` | string | no | Customer state. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {}
      ],
      "errorMessage": "string",
      "errorRaised": "string",
      "errorType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> | Customer records returned by HirePOS after the create request. |
| `errorMessage` | string | HirePOS error message when the customer create request fails. |
| `errorRaised` | string | Whether HirePOS raised an error for the customer create request. |
| `errorType` | string | HirePOS error type when the customer create request fails. |

## Native endpoint

Through the native HirePOS API, this operation is `POST /Customers` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

