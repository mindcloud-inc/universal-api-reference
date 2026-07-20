# Google Workspace Admin: Add Group Member

Adds a member to a Google Workspace Admin group.

```
POST https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-group-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "groupKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-group-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "groupKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliverySettings` | string | no | Optional delivery setting for email delivery to this member. |
| `email` | string | yes | Email address of the member to add. |
| `groupKey` | string | yes | Group email address, alias, or unique ID. |
| `role` | string | no | Role to assign: OWNER, MANAGER, or MEMBER. |
| `type` | string | no | Member type such as USER or GROUP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliverySettings": "string",
      "email": "ava@example.com",
      "etag": "string",
      "id": "string",
      "kind": "string",
      "role": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliverySettings` | string |  |
| `email` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `role` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `POST /admin/directory/v1/groups/:groupKey/members` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-group-member.md) for the provider-specific parameters and requirements.

