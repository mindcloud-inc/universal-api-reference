# DeployHQ: List Integrations

Retrieves project integrations from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-integrations?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-integrations?${params}`, {
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
| `projectId` | string | yes | The identifier or permalink of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "hook_type": "string",
      "identifier": "string",
      "name": "Ava Chen",
      "send_on_completion": true,
      "send_on_failure": true,
      "send_on_start": true,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `hook_type` | string |  |
| `identifier` | string |  |
| `name` | string |  |
| `send_on_completion` | boolean |  |
| `send_on_failure` | boolean |  |
| `send_on_start` | boolean |  |
| `updated_at` | date |  |

## Native endpoint

Through the native DeployHQ API, this operation is `GET /projects/:project_id/integrations` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

