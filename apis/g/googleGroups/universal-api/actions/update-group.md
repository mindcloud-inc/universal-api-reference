# Google Groups: Update Group

Replaces an existing group in Google Groups.

```
PUT https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupKey` | string | yes | The group email address, group alias, or unique group ID. |
| `email` | string | no | The group's primary email address. |
| `name` | string | no | The group's display name. |
| `description` | string | no | An optional description for the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminCreated": true,
      "description": "string",
      "email": "ava@example.com",
      "etag": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminCreated` | boolean |  |
| `description` | string |  |
| `email` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Google Groups API, this operation is `PUT https://admin.googleapis.com/admin/directory/v1/groups/:groupKey` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

