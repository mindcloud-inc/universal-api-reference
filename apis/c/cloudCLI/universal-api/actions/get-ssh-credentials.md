# Cloud CLI: Get SSH Credentials

Retrieves SSH credentials for a Cloud CLI environment.

```
GET https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/get-ssh-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud CLI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/get-ssh-credentials?connectionId=$CONNECTION_ID&id=46ce370c-f611-40e0-9764-ed0032dc76fa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "46ce370c-f611-40e0-9764-ed0032dc76fa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/get-ssh-credentials?${params}`, {
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
| `id` | string | yes | Environment ID. Example: `46ce370c-f611-40e0-9764-ed0032dc76fa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessUrl": "https://example.com",
      "password": "string",
      "sshCommand": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessUrl` | string |  |
| `password` | string |  |
| `sshCommand` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Cloud CLI API, this operation is `GET /environments/:id/credentials` (base URL `https://cloudcli.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ssh-credentials.md) for the provider-specific parameters and requirements.

