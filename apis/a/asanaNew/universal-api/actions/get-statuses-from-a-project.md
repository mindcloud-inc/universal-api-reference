# Asana: Get statuses from a project

Retrieves project statuses from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-statuses-from-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-statuses-from-a-project?connectionId=$CONNECTION_ID&projectGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-statuses-from-a-project?${params}`, {
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
| `limit` | number | no |  |
| `offset` | string | no |  |
| `optFields[]` | array | no |  |
| `optPretty` | boolean | no |  |
| `projectGid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "resourceType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `resourceType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET projects/:project_gid/project_statuses` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statuses-from-a-project.md) for the provider-specific parameters and requirements.

