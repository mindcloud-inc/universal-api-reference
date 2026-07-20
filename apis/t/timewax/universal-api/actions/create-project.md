# Timewax: Create Project

Creates a new project in Timewax.

```
POST https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.project.code": "string",
  "request.project.name": "Ava Chen",
  "request.project.company": "string",
  "request.project.organisationalUnit": "string",
  "request.project.projectManager": "string",
  "request.project.currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.project.code": "string",
    "request.project.name": "Ava Chen",
    "request.project.company": "string",
    "request.project.organisationalUnit": "string",
    "request.project.projectManager": "string",
    "request.project.currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.project.code` | string | yes | Code of the project. |
| `request.project.name` | string | yes | Name of the project. |
| `request.project.company` | string | yes | Code or name of the client. |
| `request.project.organisationalUnit` | string | yes | Code or name of the department. |
| `request.project.projectManager` | string | yes | Code or name of the project manager. |
| `request.project.currency` | string | yes | Project currency. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | string | Operation validity indicator. |

## Native endpoint

Through the native Timewax API, this operation is `POST project/add/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

