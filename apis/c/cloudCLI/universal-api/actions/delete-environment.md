# Cloud CLI: Delete Environment

Deletes an existing environment from Cloud CLI.

```
DELETE https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/delete-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud CLI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/delete-environment?connectionId=$CONNECTION_ID&id=46ce370c-f611-40e0-9764-ed0032dc76fa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "46ce370c-f611-40e0-9764-ed0032dc76fa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/delete-environment?${params}`, {
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
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAt` | date |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloud CLI API, this operation is `DELETE /environments/:id` (base URL `https://cloudcli.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-environment.md) for the provider-specific parameters and requirements.

