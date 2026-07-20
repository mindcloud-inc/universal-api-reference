# GoTeamup: Update Customer

Updates an existing customer in GoTeamup.

```
PUT https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | Updated customer first name |
| `id` | number | yes | The TeamUp customer ID |
| `lastName` | string | no | Customer last name. |
| `visibility` | string | no | Customer visibility status. |
| `status` | string | no | Customer status. |
| `isStatusLocked` | boolean | no | Whether the customer status is locked. |

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

Through the native GoTeamup API, this operation is `PATCH /customers/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

