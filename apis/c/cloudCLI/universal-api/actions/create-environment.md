# Cloud CLI: Create Environment

Creates a new environment in Cloud CLI.

```
POST https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/create-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud CLI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/create-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "My Backend API",
  "subdomain": "mybackend-abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/create-environment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "My Backend API",
    "subdomain": "mybackend-abc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new environment. Example: `My Backend API`. |
| `subdomain` | string | yes | Unique subdomain slug for the environment. Example: `mybackend-abc123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `githubUrl` | string | no | GitHub repository URL to clone into the environment. Example: `https://github.com/username/repo`. |
| `githubToken` | string | no | GitHub personal access token for private repositories. Example: `ghp_xxxxxxxxxxxx`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "githubUrl": "https://example.com",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string",
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessUrl` | string |  |
| `createdAt` | date |  |
| `githubUrl` | string |  |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `status` | string |  |
| `subdomain` | string |  |

## Native endpoint

Through the native Cloud CLI API, this operation is `POST /environments` (base URL `https://cloudcli.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-environment.md) for the provider-specific parameters and requirements.

