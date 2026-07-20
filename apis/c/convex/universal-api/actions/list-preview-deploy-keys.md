# Convex: List Preview Deploy Keys

Retrieves preview deploy keys from a Convex project.

```
GET https://connect.mindcloud.co/v1/universal/convex/latest/actions/list-preview-deploy-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/list-preview-deploy-keys?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/list-preview-deploy-keys?${params}`, {
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
| `projectId` | number | yes | The Convex project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items` | array<object> |  |

## Native endpoint

Through the native Convex API, this operation is `GET /projects/:project_id/list_preview_deploy_keys` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-preview-deploy-keys.md) for the provider-specific parameters and requirements.

