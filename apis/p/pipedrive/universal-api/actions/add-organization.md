# Pipedrive: Add Organization

Creates a new organization in Pipedrive.

```
POST https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the organization. |
| `ownerId` | number | no | Owner user ID for the organization. |
| `address` | object | no | Address object for the organization. |
| `labelIds` | list<number> | no | Label IDs to assign to the organization. |
| `visibleTo` | string | no | Visibility setting for the organization record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "addTime": "string",
      "annualRevenue": {},
      "customFields": {},
      "employeeCount": {},
      "id": 1,
      "industry": {},
      "isDeleted": true,
      "linkedin": {},
      "name": "Ava Chen",
      "ownerId": 1,
      "updateTime": {},
      "visibleTo": 1,
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `addTime` | string |  |
| `annualRevenue` | object |  |
| `customFields` | object |  |
| `employeeCount` | object |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | boolean |  |
| `linkedin` | object |  |
| `name` | string |  |
| `ownerId` | number |  |
| `updateTime` | object |  |
| `visibleTo` | number |  |
| `website` | object |  |

## Native endpoint

Through the native Pipedrive API, this operation is `POST v2/organizations` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-organization.md) for the provider-specific parameters and requirements.

