# Gridly: Get Project

Retrieves a project from Gridly by project ID.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | ID can be found in the URL of the web application: app.gridly.com/projects/<id>. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "databases": [
        {}
      ],
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number | Owning company ID. |
| `databases` | array<object> | Databases in the project. |
| `description` | string | Project description. |
| `id` | number | Project ID. |
| `name` | string | Project name. |
| `type` | string | Project type. |

## Native endpoint

Through the native Gridly API, this operation is `GET /projects/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

