# DeployHQ: List Deployments

Retrieves deployments for a project from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-deployments?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/list-deployments?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentlyRunning` | boolean | no | Filter to currently running deployments. Set to 1 to enable. |
| `to` | string | no | Filter deployments by parent identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `records` | array<object> |  |

## Native endpoint

Through the native DeployHQ API, this operation is `GET /projects/:project_id/deployments` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deployments.md) for the provider-specific parameters and requirements.

