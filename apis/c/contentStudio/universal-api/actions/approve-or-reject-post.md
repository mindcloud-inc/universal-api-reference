# ContentStudio: Approve or Reject Post

Approves or rejects a post under review in ContentStudio.

```
PUT https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/approve-or-reject-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/approve-or-reject-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "post_id": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/approve-or-reject-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "post_id": "string",
    "workspace_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Approval action to perform. |
| `comment` | string | no | Optional approval comment. |
| `post_id` | string | yes | ContentStudio post ID. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native ContentStudio API, this operation is `POST /workspaces/:workspace_id/posts/:post_id/approval` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-or-reject-post.md) for the provider-specific parameters and requirements.

