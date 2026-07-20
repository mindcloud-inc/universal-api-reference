# Cloud CLI: List Environments

Retrieves environments from Cloud CLI.

```
GET https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud CLI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/list-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/list-environments?${params}`, {
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
| `status` | string | no | Optional environment status to match. One of: `0`, `1`, `2`, `3`, `4`. Example: `running`. |

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
| `name` | string |  |
| `status` | string |  |
| `subdomain` | string |  |

## Native endpoint

Through the native Cloud CLI API, this operation is `GET /environments` (base URL `https://cloudcli.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

