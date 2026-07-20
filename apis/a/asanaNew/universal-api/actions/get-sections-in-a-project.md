# Asana: Get sections in a project

Retrieves sections in a project from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-sections-in-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-sections-in-a-project?connectionId=$CONNECTION_ID&limit=25&offset=0&projectGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-sections-in-a-project?${params}`, {
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
| `projectGid` | string | yes | Path parameter: project_gid |
| `offset` | string | no |  |
| `optFields[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "name": "Ava Chen",
      "resourceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `name` | string |  |
| `resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `GET projects/:project_gid/sections` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-sections-in-a-project.md) for the provider-specific parameters and requirements.

