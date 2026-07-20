# LogSnag: Group User



```
PUT https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/group-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogSnag `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/group-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "groupId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/group-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "groupId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name in LogSnag. |
| `groupId` | string | yes | Group identifier to associate or update. |
| `userId` | string | yes | User identifier to associate with the group. |
| `properties` | object | no | Optional group properties as key/value pairs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "project": "string",
      "properties": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string | Group identifier. |
| `project` | string | LogSnag project name. |
| `properties` | object | Applied group properties. |
| `userId` | string | User identifier associated with the group. |

## Native endpoint

Through the native LogSnag API, this operation is `POST /group` (base URL `https://api.logsnag.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/group-user.md) for the provider-specific parameters and requirements.

