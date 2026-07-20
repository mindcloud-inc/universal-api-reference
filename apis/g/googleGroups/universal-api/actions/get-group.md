# Google Groups: Get Group

Retrieves a Google Group by key.

```
GET https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/get-group?connectionId=$CONNECTION_ID&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/get-group?${params}`, {
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
      "adminCreated": true,
      "description": "string",
      "directMembersCount": "string",
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
| `directMembersCount` | string |  |
| `email` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Google Groups API, this operation is `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

