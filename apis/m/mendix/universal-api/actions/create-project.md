# Mendix: Create Project

Creates a new project in Mendix and returns a job.

```
POST https://connect.mindcloud.co/v1/universal/mendix/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Customer Portal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendix/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Customer Portal"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the project. Example: `Customer Portal`. |
| `summary` | string | no | Description of the project. Example: `Customer self-service portal`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | no | Identifier of the template that the project will be copied from. If empty, Mendix uses the default template. |
| `image` | string | no | Base64-encoded project icon image. Mendix limits the file size and image dimensions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique identifier of the project creation job. |

## Native endpoint

Through the native Mendix API, this operation is `POST /projects` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

