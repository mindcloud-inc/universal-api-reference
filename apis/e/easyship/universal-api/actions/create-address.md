# Easyship: Create Address

Creates a new address in Easyship.

```
POST https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "line1": "string",
  "city": "string",
  "companyName": "Ava Chen",
  "contactName": "Ava Chen",
  "contactEmail": "ava@example.com",
  "contactPhone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "line1": "string",
    "city": "string",
    "companyName": "Ava Chen",
    "contactName": "Ava Chen",
    "contactEmail": "ava@example.com",
    "contactPhone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `line1` | string | yes | First address line. |
| `line2` | string | no | Second address line. |
| `city` | string | yes | Address city. |
| `state` | string | no | Address state or province. |
| `postalCode` | string | no | Address postal code. |
| `countryAlpha2` | string | no | Two-letter country code. |
| `companyName` | string | yes | Company name on the address. |
| `contactName` | string | yes | Contact full name. |
| `contactEmail` | string | yes | Contact email address. |
| `contactPhone` | string | yes | Contact phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "companyName": "Ava Chen",
      "contactEmail": "ava@example.com",
      "contactName": "Ava Chen",
      "contactPhone": "string",
      "countryAlpha2": "string",
      "id": "string",
      "line1": "string",
      "line2": "string",
      "postalCode": "string",
      "state": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `companyName` | string |  |
| `contactEmail` | string |  |
| `contactName` | string |  |
| `contactPhone` | string |  |
| `countryAlpha2` | string |  |
| `id` | string |  |
| `line1` | string |  |
| `line2` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `POST /addresses` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-address.md) for the provider-specific parameters and requirements.

