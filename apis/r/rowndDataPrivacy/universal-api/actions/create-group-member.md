# Rownd Data Privacy: Create Group Member



```
POST https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group` | string | yes | Rownd group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group_id": "string",
      "id": "string",
      "roles": [
        "string"
      ],
      "state": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group_id` | string | Rownd group identifier. |
| `id` | string | Group member identifier. |
| `roles` | array<string> | Roles granted to the member. |
| `state` | string | Membership state. |
| `user_id` | string | Rownd user identifier. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `POST /groups/:group/members` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-member.md) for the provider-specific parameters and requirements.

