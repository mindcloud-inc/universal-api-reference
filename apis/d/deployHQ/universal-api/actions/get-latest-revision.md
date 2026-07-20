# DeployHQ: Get Latest Revision

Retrieves the latest repository revision from DeployHQ.

```
GET https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-latest-revision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeployHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-latest-revision?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deployHQ/latest/actions/get-latest-revision?${params}`, {
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
| `branch` | string | no | The branch name to get the latest revision for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `update` | boolean | no | Set to 1 to update the repository before getting the latest revision. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ref": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ref` | string |  |

## Native endpoint

Through the native DeployHQ API, this operation is `GET /projects/:project_id/repository/latest_revision` (base URL `https://{{credentials.account}}.deployhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-revision.md) for the provider-specific parameters and requirements.

