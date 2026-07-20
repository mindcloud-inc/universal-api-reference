# Bookvault: Create Address

Creates a new address in Bookvault.

```
POST https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/create-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | object | yes | Address payload to create in Bookvault. Required fields include Addressee, Address1, Town, and County. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address1": "string",
      "Addressee": "string",
      "CommonAddrID": 1,
      "Company": "string",
      "Country": {},
      "Email": "ava@example.com",
      "Postcode": "string",
      "Town": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address1` | string |  |
| `Addressee` | string |  |
| `CommonAddrID` | number |  |
| `Company` | string |  |
| `Country` | object |  |
| `Email` | string |  |
| `Postcode` | string |  |
| `Town` | string |  |

## Native endpoint

Through the native Bookvault API, this operation is `POST /Addresses` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-address.md) for the provider-specific parameters and requirements.

