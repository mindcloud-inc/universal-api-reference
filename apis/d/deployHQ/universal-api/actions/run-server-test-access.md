# DeployHQ: Run Server Test Access

Runs a server access test in DeployHQ.

```
POST https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/run-server-test-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/run-server-test-access" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "serverId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/run-server-test-access', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "serverId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The identifier or permalink of the project. |
| `serverId` | string | yes | ID of the server to test. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "identifier": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `identifier` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `POST /projects/:project_id/servers/:server_id/test_access` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-server-test-access.md) for the provider-specific parameters and requirements.

