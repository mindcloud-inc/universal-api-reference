# Leantime: List Comments



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-comments?connectionId=$CONNECTION_ID&params.module=project&entityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.module": "project",
  "entityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-comments?${params}`, {
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
| `params.module` | string | yes | The Leantime module name. Default: `project`. |
| `entityId` | number | yes | The target entity id. |
| `params.commentOrder` | number | no | 0 for oldest-first or 1 for newest-first. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentParent": 1,
      "date": "string",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "moduleId": 1,
      "profileId": "string",
      "rawDate": "string",
      "status": "string",
      "text": "string",
      "userId": 1,
      "userModified": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentParent` | number |  |
| `date` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `moduleId` | number |  |
| `profileId` | string |  |
| `rawDate` | string |  |
| `status` | string |  |
| `text` | string |  |
| `userId` | number |  |
| `userModified` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

