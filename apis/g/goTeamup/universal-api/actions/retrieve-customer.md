# GoTeamup: Retrieve Customer

Retrieves a customer from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-customer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-customer?${params}`, {
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
| `id` | number | yes | The TeamUp customer ID |

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

Through the native GoTeamup API, this operation is `GET /customers/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer.md) for the provider-specific parameters and requirements.

