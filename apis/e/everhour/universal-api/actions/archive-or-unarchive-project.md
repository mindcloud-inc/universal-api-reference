# Everhour: Archive or Unarchive Project

Archives or unarchives a project in Everhour.

```
PUT https://connect.mindcloud.co/v1/universal/everhour/latest/actions/archive-or-unarchive-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/archive-or-unarchive-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "archived": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everhour/latest/actions/archive-or-unarchive-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "archived": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Everhour project ID. |
| `archived` | boolean | yes | Whether the project should be archived. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {}
      ],
      "billing": {},
      "budget": {},
      "canSyncTasks": true,
      "changeProtected": true,
      "client": 1,
      "connectionStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "editable": true,
      "enableResourcePlanner": true,
      "estimatesType": "string",
      "favorite": true,
      "foreign": true,
      "hasWebhook": true,
      "id": "string",
      "isTemplate": true,
      "name": "Ava Chen",
      "platform": "string",
      "privacy": "string",
      "rate": {},
      "status": "string",
      "type": "string",
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<object> |  |
| `billing` | object |  |
| `budget` | object |  |
| `canSyncTasks` | boolean |  |
| `changeProtected` | boolean |  |
| `client` | number |  |
| `connectionStatus` | string |  |
| `createdAt` | date |  |
| `editable` | boolean |  |
| `enableResourcePlanner` | boolean |  |
| `estimatesType` | string |  |
| `favorite` | boolean |  |
| `foreign` | boolean |  |
| `hasWebhook` | boolean |  |
| `id` | string |  |
| `isTemplate` | boolean |  |
| `name` | string |  |
| `platform` | string |  |
| `privacy` | string |  |
| `rate` | object |  |
| `status` | string |  |
| `type` | string |  |
| `users` | array<number> |  |

## Native endpoint

Through the native Everhour API, this operation is `PATCH /projects/:projectId/archive` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-or-unarchive-project.md) for the provider-specific parameters and requirements.

