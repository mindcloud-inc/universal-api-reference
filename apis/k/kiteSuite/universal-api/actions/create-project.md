# KiteSuite: Create Project

Creates a new project in KiteSuite.

```
POST https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectName": "Ava Chen",
  "projectType": "string",
  "projectLead": "string",
  "avatar": "default.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectName": "Ava Chen",
    "projectType": "string",
    "projectLead": "string",
    "avatar": "default.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectName` | string | yes | Project name. |
| `projectType` | string | yes | Project type such as agile. |
| `projectLead` | string | yes | User ID of the project lead. |
| `avatar` | string | yes | Project avatar filename. Default: `default.png`. |
| `description` | string | no | Project description. |
| `members[]` | array<string> | no | Email addresses to add to the project. Pass an array of emails. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {}
      ],
      "epics": [
        {}
      ],
      "itemTypes": [
        {}
      ],
      "lists": [
        {}
      ],
      "project": {},
      "sprints": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> |  |
| `epics` | array<object> |  |
| `itemTypes` | array<object> |  |
| `lists` | array<object> |  |
| `project` | object |  |
| `sprints` | array<object> |  |

## Native endpoint

Through the native KiteSuite API, this operation is `POST /api/v1/project` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

