# GoTeamup: Create Customer

Creates a new customer in GoTeamup.

```
POST https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Customer first name |
| `lastName` | string | yes | Customer last name |
| `email` | string | yes | Customer email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "email": "ava@example.com",
      "family": {},
      "familyRole": {},
      "firstName": "Ava",
      "id": 1,
      "image": {},
      "isLead": true,
      "isStatusLocked": true,
      "lastName": "Chen",
      "leadSource": {},
      "object": "string",
      "participating": true,
      "provider": 1,
      "referralCode": {
        "code": "string",
        "shareUrl": "https://example.com"
      },
      "status": {},
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `email` | string |  |
| `family` | object |  |
| `familyRole` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `image` | object |  |
| `isLead` | boolean |  |
| `isStatusLocked` | boolean |  |
| `lastName` | string |  |
| `leadSource` | object |  |
| `object` | string |  |
| `participating` | boolean |  |
| `provider` | number |  |
| `referralCode.code` | string |  |
| `referralCode.shareUrl` | string |  |
| `status` | object |  |
| `visibility` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `POST /customers` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

