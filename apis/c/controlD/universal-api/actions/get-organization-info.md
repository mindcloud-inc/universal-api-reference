# Control D: Get Organization Info

Retrieves organization details from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-organization-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-organization-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-organization-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "contact_email": "ava@example.com",
      "date": "string",
      "max_legacy_resolvers": 1,
      "max_profiles": 1,
      "max_routers": 1,
      "max_sub_orgs": 1,
      "max_users": 1,
      "members": {},
      "name": "Ava Chen",
      "PK": "string",
      "price_routers": 1,
      "price_users": 1,
      "profiles": {},
      "routers": {},
      "stats_endpoint": "string",
      "status": 1,
      "sub_organizations": {},
      "users": {},
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `contact_email` | string |  |
| `date` | string |  |
| `max_legacy_resolvers` | number |  |
| `max_profiles` | number |  |
| `max_routers` | number |  |
| `max_sub_orgs` | number |  |
| `max_users` | number |  |
| `members` | object |  |
| `name` | string |  |
| `PK` | string |  |
| `price_routers` | number |  |
| `price_users` | number |  |
| `profiles` | object |  |
| `routers` | object |  |
| `stats_endpoint` | string |  |
| `status` | number |  |
| `sub_organizations` | object |  |
| `users` | object |  |
| `website` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /organizations/organization` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-info.md) for the provider-specific parameters and requirements.

