# Pipedrive: Update Organization

Updates an existing organization in Pipedrive.

```
PUT https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-organization', {
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
| `id` | number | yes | Unique ID of the organization to update. |
| `name` | string | no | Updated organization name. |
| `ownerId` | number | no | Updated owner user ID. |
| `address` | object | no | Updated address object for the organization. |
| `labelIds` | list<number> | no | Updated label IDs for the organization. |
| `visibleTo` | string | no | Updated visibility setting. |

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
      "updateTime": "string",
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
| `updateTime` | string |  |
| `visibleTo` | number |  |
| `website` | object |  |

## Native endpoint

Through the native Pipedrive API, this operation is `PATCH v2/organizations/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

