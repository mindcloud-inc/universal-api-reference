# Google Workspace Admin: Update Group Member

Updates a member in a Google Workspace Admin group.

```
PUT https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-group-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "string",
  "memberKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-group-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupKey": "string",
    "memberKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliverySettings` | string | no | Optional delivery setting for email delivery to this member. |
| `groupKey` | string | yes | Group email address, alias, or unique ID. |
| `memberKey` | string | yes | Member email address, alias, or unique ID. |
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

Through the native Google Workspace Admin API, this operation is `PUT /admin/directory/v1/groups/:groupKey/members/:memberKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-member.md) for the provider-specific parameters and requirements.

