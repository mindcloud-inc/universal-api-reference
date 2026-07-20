# Zoho Connect: Add User to a Group

Adds users to a group in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-user-to-a-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-user-to-a-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "partitionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-user-to-a-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "partitionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes | Network ID. |
| `partitionId` | string | yes | Group ID. |
| `memberIds` | string<string> | no | User IDs separated by a comma. Accepts multiple values as an array. |
| `adminIds` | string<string> | no | Comma-separated IDs of users to add as admins. Accepts multiple values as an array. |
| `userEmailIds` | string<string> | no | Users' email addresses separated by a comma. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addUsersToGroup` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-a-group.md) for the provider-specific parameters and requirements.

