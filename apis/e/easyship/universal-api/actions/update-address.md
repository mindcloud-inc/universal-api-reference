# Easyship: Update Address

Updates an existing address in Easyship.

```
PUT https://connect.mindcloud.co/v1/universal/easyship/latest/actions/update-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/update-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/update-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressId` | string | yes | The Easyship address ID. |
| `line1` | string | no | First address line. |
| `line2` | string | no | Second address line. |
| `city` | string | no | Address city. |
| `state` | string | no | Address state or province. |
| `postalCode` | string | no | Address postal code. |
| `countryAlpha2` | string | no | Two-letter country code. |
| `companyName` | string | no | Company name on the address. |
| `contactName` | string | no | Contact full name. |
| `contactEmail` | string | no | Contact email address. |
| `contactPhone` | string | no | Contact phone number. |

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

Through the native Easyship API, this operation is `PATCH /addresses/:address_id` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-address.md) for the provider-specific parameters and requirements.

