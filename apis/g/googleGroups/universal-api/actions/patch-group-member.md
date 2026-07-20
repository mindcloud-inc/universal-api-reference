# Google Groups: Patch Group Member

Updates an existing group member in Google Groups.

```
PUT https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/patch-group-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/patch-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "string",
  "memberKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/patch-group-member', {
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
| `groupKey` | string | yes | The group email address, group alias, or unique group ID. |
| `memberKey` | string | yes | The member email address or unique member ID. |
| `role` | string | no | The member's role in the group, such as MEMBER, MANAGER, or OWNER. |
| `deliverySettings` | string | no | Email delivery preference for the member, such as ALL_MAIL, DAILY, DIGEST, DISABLED, or NONE. |

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

Through the native Google Groups API, this operation is `PATCH https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-group-member.md) for the provider-specific parameters and requirements.

