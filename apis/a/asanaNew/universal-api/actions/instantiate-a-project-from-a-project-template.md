# Asana: Instantiate a project from a project template

Creates a project from an Asana project template.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/instantiate-a-project-from-a-project-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/instantiate-a-project-from-a-project-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectTemplateGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/instantiate-a-project-from-a-project-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectTemplateGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataIsStrict` | boolean | no |  |
| `dataName` | string | no |  |
| `dataPublic` | boolean | no |  |
| `dataRequestedDates][]` | array | no |  |
| `dataRequestedDatesGid` | string | no |  |
| `dataRequestedDatesValue` | date | no |  |
| `dataTeam` | string | no |  |
| `dataWorkspace` | string | no |  |
| `projectTemplateGid` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optPretty` | boolean | no |  |
| `optFields` | list<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST project_templates/:project_template_gid/instantiateProject` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/instantiate-a-project-from-a-project-template.md) for the provider-specific parameters and requirements.

