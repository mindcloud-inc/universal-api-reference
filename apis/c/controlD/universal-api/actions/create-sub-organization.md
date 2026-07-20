# Control D: Create Sub-Organization

Creates a sub-organization in Control D.

```
POST https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-sub-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-sub-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "contactEmail": "ava@example.com",
  "twofaReq": 1,
  "statsEndpoint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-sub-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "contactEmail": "ava@example.com",
    "twofaReq": 1,
    "statsEndpoint": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | (Required) Organization name |
| `contactEmail` | string | yes | Primary contact email for this sub-organization. |
| `twofaReq` | number | yes | Whether 2FA/MFA is required for members of this organization. 0 = no, 1 = yes. |
| `statsEndpoint` | string | yes | Primary key of the desired storage region. See List Storage Regions. |
| `address` | string | no | Physical address of this organization. |
| `website` | string | no | Website URL of this organization. |
| `contactName` | string | no | Contact name for the person responsible for this organization. |
| `contactPhone` | string | no | Phone number associated with this organization. |
| `parentProfile` | string | no | Global profile ID to enforce on all created devices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "contact_email": "ava@example.com",
      "contact_name": "Ava Chen",
      "contact_phone": "string",
      "date": "string",
      "max_legacy_resolvers": 1,
      "max_profiles": 1,
      "max_routers": 1,
      "max_users": 1,
      "members": {},
      "name": "Ava Chen",
      "parent_org": {},
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
| `contact_phone` | string |  |
| `date` | string |  |
| `max_legacy_resolvers` | number |  |
| `max_profiles` | number |  |
| `max_routers` | number |  |
| `max_users` | number |  |
| `members` | object |  |
| `name` | string |  |
| `parent_org` | object |  |
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

Through the native Control D API, this operation is `POST /organizations/suborg` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sub-organization.md) for the provider-specific parameters and requirements.

