# Google Groups: List Group Members

Retrieves members of a group from Google Groups.

```
GET https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-group-members?connectionId=$CONNECTION_ID&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/list-group-members?${params}`, {
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
| `groupKey` | string | yes | The group email address, group alias, or unique group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `email` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `role` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Groups API, this operation is `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-members.md) for the provider-specific parameters and requirements.

