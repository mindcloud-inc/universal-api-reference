# Cloud CLI: Start Environment

Starts an existing environment in Cloud CLI.

```
PUT https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/start-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud CLI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/start-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "46ce370c-f611-40e0-9764-ed0032dc76fa"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/start-environment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "46ce370c-f611-40e0-9764-ed0032dc76fa"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Environment ID. Example: `46ce370c-f611-40e0-9764-ed0032dc76fa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Cloud CLI API, this operation is `POST /environments/:id/start` (base URL `https://cloudcli.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-environment.md) for the provider-specific parameters and requirements.

