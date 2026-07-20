# Control D: List Sub-Organizations



```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-sub-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-sub-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-sub-organizations?${params}`, {
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
      "contact_name": "Ava Chen",
      "date": "string",
      "max_legacy_resolvers": 1,
      "max_profiles": 1,
      "max_routers": 1,
      "max_users": 1,
      "members": {},
      "name": "Ava Chen",
      "parent_org": {},
      "parent_profile": {},
      "PK": "string",
      "profiles": {},
      "routers": {},
      "stats_endpoint": "string",
      "status": 1,
      "sub_organizations": {},
      "twofa_req": 1,
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
| `contact_name` | string |  |
| `date` | string |  |
| `max_legacy_resolvers` | number |  |
| `max_profiles` | number |  |
| `max_routers` | number |  |
| `max_users` | number |  |
| `members` | object |  |
| `name` | string |  |
| `parent_org` | object |  |
| `parent_profile` | object |  |
| `PK` | string |  |
| `profiles` | object |  |
| `routers` | object |  |
| `stats_endpoint` | string |  |
| `status` | number |  |
| `sub_organizations` | object |  |
| `twofa_req` | number |  |
| `users` | object |  |
| `website` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /organizations/sub_organizations` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sub-organizations.md) for the provider-specific parameters and requirements.

