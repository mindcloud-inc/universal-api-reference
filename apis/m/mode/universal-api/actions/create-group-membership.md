# Mode: Create Group Membership

Add a member to a group in a Mode workspace.

```
POST https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-group-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupToken": "string",
  "membership": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-group-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupToken": "string",
    "membership": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupToken` | string | yes | Mode group token. |
| `membership` | object | yes | Membership fields to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Links": {},
      "memberToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Links` | object | Mode HAL links. |
| `memberToken` | string | Mode member token. |
| `token` | string | Mode group membership token. |

## Native endpoint

Through the native Mode API, this operation is `POST /groups/[:groupToken]/memberships` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-membership.md) for the provider-specific parameters and requirements.

