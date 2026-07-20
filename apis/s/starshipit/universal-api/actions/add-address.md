# Starshipit: Add Address



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/add-address', {
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
| `address.code` | string | no |  |
| `address.name` | string | no |  |
| `address.company` | string | no |  |
| `address.postCode` | string | no |  |
| `address.street` | string | no |  |
| `address.suburb` | string | no |  |
| `address.city` | string | no |  |
| `address.state` | string | no |  |
| `address.country` | string | no |  |
| `address.phone` | string | no |  |
| `address.instructions` | string | no |  |
| `address.building` | string | no |  |
| `address.email` | string | no |  |
| `address.carrier` | number | no |  |
| `address.signatureRequired` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "building": "string",
        "carrier": 1,
        "city": "string",
        "code": "string",
        "company": "string",
        "country": "string",
        "email": "ava@example.com",
        "instructions": "string",
        "name": "Ava Chen",
        "phone": "string",
        "postCode": "string",
        "signatureRequired": true,
        "state": "string",
        "street": "string",
        "suburb": "string"
      },
      "errors": [
        "string"
      ],
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.building` | string |  |
| `address.carrier` | number |  |
| `address.city` | string |  |
| `address.code` | string |  |
| `address.company` | string |  |
| `address.country` | string |  |
| `address.email` | string |  |
| `address.instructions` | string |  |
| `address.name` | string |  |
| `address.phone` | string |  |
| `address.postCode` | string |  |
| `address.signatureRequired` | boolean |  |
| `address.state` | string |  |
| `address.street` | string |  |
| `address.suburb` | string |  |
| `errors` | array<string> |  |
| `id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /addressbook/` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-address.md) for the provider-specific parameters and requirements.

