# Asana: Duplicate a project

Duplicates a project in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/duplicate-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/duplicate-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectGid": "string",
  "data.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/duplicate-a-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectGid": "string",
    "data.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataInclude` | string | no |  |
| `dataName` | string | no |  |
| `dataScheduleDatesDueOn` | string | no |  |
| `dataScheduleDatesShouldSkipWeekends` | boolean | no |  |
| `dataScheduleDatesStartOn` | string | no |  |
| `dataTeam` | string | no |  |
| `projectGid` | string | yes | Asana project gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |
| `data.name` | string | yes | Asana name parameter. |
| `data.team` | string | no | Asana team parameter. |
| `data.include` | string | no | Asana include parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "newProject": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "resourceSubtype": "string",
      "resourceType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `newProject.gid` | string |  |
| `newProject.name` | string |  |
| `newProject.resourceType` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST projects/:project_gid/duplicate` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-a-project.md) for the provider-specific parameters and requirements.

