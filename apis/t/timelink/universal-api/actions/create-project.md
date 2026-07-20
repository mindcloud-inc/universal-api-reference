# Timelink: Create Project

Creates a project in the Timelink workspace.

```
POST https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-project', {
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
| `name` | string | yes |  |
| `client_id` | string | no |  |
| `ext_tool_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acronym": {},
      "active": true,
      "billable": true,
      "client": {
        "acronym": {},
        "active": true,
        "activeProjectsCount": 1,
        "billable": true,
        "color": "string",
        "companyId": "string",
        "createdAt": "string",
        "demoFlag": true,
        "extToolId": "string",
        "id": "string",
        "imageId": {},
        "info": {},
        "lastSync": {},
        "name": "Ava Chen",
        "projectsCount": 1,
        "updatedAt": "string"
      },
      "clientId": "string",
      "color": "string",
      "createdAt": "string",
      "demoFlag": true,
      "extToolId": "string",
      "id": "string",
      "imageId": {},
      "info": {},
      "lastSync": {},
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acronym` | object |  |
| `active` | boolean |  |
| `billable` | boolean |  |
| `client.acronym` | object |  |
| `client.active` | boolean |  |
| `client.activeProjectsCount` | number |  |
| `client.billable` | boolean |  |
| `client.color` | string |  |
| `client.companyId` | string |  |
| `client.createdAt` | string |  |
| `client.demoFlag` | boolean |  |
| `client.extToolId` | string |  |
| `client.id` | string |  |
| `client.imageId` | object |  |
| `client.info` | object |  |
| `client.lastSync` | object |  |
| `client.name` | string |  |
| `client.projectsCount` | number |  |
| `client.updatedAt` | string |  |
| `clientId` | string |  |
| `color` | string |  |
| `createdAt` | string |  |
| `demoFlag` | boolean |  |
| `extToolId` | string |  |
| `id` | string |  |
| `imageId` | object |  |
| `info` | object |  |
| `lastSync` | object |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `POST /projects` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

