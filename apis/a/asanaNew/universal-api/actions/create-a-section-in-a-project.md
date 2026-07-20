# Asana: Create a section in a project

Creates a section in a project in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-section-in-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-section-in-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataName": "Ava Chen",
  "projectGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-section-in-a-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataName": "Ava Chen",
    "projectGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataInsertAfter` | string | no |  |
| `dataInsertBefore` | string | no |  |
| `dataName` | string | yes |  |
| `projectGid` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optPretty` | boolean | no |  |
| `optFields` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "gid": "string",
      "name": "Ava Chen",
      "project": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `gid` | string |  |
| `name` | string |  |
| `project.gid` | string |  |
| `project.name` | string |  |
| `project.resourceType` | string |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST projects/:project_gid/sections` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-section-in-a-project.md) for the provider-specific parameters and requirements.

