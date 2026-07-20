# Google Groups: Create Group Alias

Creates a group alias in Google Groups.

```
POST https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/create-group-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/create-group-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "string",
  "alias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/create-group-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupKey": "string",
    "alias": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupKey` | string | yes | The group email address, group alias, or unique group ID. |
| `alias` | string | yes | The editable alias email address to add to the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "etag": "string",
      "id": "string",
      "kind": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |

## Native endpoint

Through the native Google Groups API, this operation is `POST https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-alias.md) for the provider-specific parameters and requirements.

