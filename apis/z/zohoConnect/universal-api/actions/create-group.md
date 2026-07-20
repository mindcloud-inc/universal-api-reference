# Zoho Connect: Create Group

Creates a new group in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes | Network ID. |
| `name` | string | yes | Provide a name for the group. |
| `desc` | string | no | Add a description. |
| `userIds` | string<string> | no | User IDs separated by a comma. Accepts multiple values as an array. |
| `isPrivate` | boolean | no | Set true if you want your group to be private. |
| `isOpenMembership` | boolean | no | Set true if members should find and join this group. |
| `fileId` | string | no | Add a group logo ID. |
| `createChannel` | boolean | no | Set true to create a channel for this group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isPublic": "string",
      "name": "Ava Chen",
      "partitionId": "string",
      "result": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isPublic` | string |  |
| `name` | string |  |
| `partitionId` | string |  |
| `result` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addGroup` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

