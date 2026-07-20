# DeployHQ: Get Repository

Retrieves the repository for a project from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-repository
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-repository?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-repository?${params}`, {
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
      "branch": "string",
      "cached": true,
      "hosting_service": {},
      "port": 1,
      "scm_type": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `cached` | boolean |  |
| `hosting_service` | object |  |
| `port` | number |  |
| `scm_type` | string |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `GET /projects/:project_id/repository` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository.md) for the provider-specific parameters and requirements.

