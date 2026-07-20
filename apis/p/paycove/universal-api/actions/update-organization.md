# Paycove: Update Organization

Updates an organization in Paycove.

```
PUT https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Paycove CRMOrganization ID. Example: `1`. |
| `name` | string | no | Organization name. Example: `Example Company`. |
| `email` | string | no | Organization email. Example: `billing@example.com`. |
| `phone` | string | no | Organization phone. Example: `+1 555 0100`. |
| `line1` | string | no | Street address. Example: `123 Main St`. |
| `city` | string | no | City. Example: `Austin`. |
| `state` | string | no | State or region. Example: `Texas`. |
| `country` | string | no | Country. Example: `US`. |
| `postalCode` | string | no | Postal code. Example: `78701`. |
| `ownerId` | string | no | Organization owner ID. Example: `11768907`. |
| `twitter` | string | no | Organization Twitter. Example: `https://x.com/example`. |
| `facebook` | string | no | Organization Facebook. Example: `https://facebook.com/example`. |
| `linkedin` | string | no | Organization LinkedIn. Example: `https://linkedin.com/company/example`. |
| `industry` | string | no | Organization industry. Example: `Software`. |
| `website` | string | no | Organization website. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "city": {},
      "country": {},
      "createdAt": "string",
      "creatorId": {},
      "crm": {},
      "crmOrganizationId": "string",
      "email": {},
      "facebook": {},
      "id": 1,
      "industry": {},
      "line1": {},
      "linkedin": {},
      "name": "Ava Chen",
      "ownerId": {},
      "phone": {},
      "postalCode": {},
      "state": {},
      "twitter": {},
      "updatedAt": "string",
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `city` | object |  |
| `country` | object |  |
| `createdAt` | string |  |
| `creatorId` | object |  |
| `crm` | object |  |
| `crmOrganizationId` | string |  |
| `email` | object |  |
| `facebook` | object |  |
| `id` | number |  |
| `industry` | object |  |
| `line1` | object |  |
| `linkedin` | object |  |
| `name` | string |  |
| `ownerId` | object |  |
| `phone` | object |  |
| `postalCode` | object |  |
| `state` | object |  |
| `twitter` | object |  |
| `updatedAt` | string |  |
| `website` | object |  |

## Native endpoint

Through the native Paycove API, this operation is `PATCH organizations/:id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

