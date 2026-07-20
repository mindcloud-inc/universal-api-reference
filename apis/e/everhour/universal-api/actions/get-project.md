# Everhour: Get Project

Retrieves a specific project from Everhour.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | Everhour project ID. |

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

Through the native Everhour API, this operation is `GET /projects/:projectId` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

