# Mode: Create Collection Membership

Add a member to a collection in a Mode workspace.

```
POST https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "space": "string",
  "membership": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "space": "string",
    "membership": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `space` | string | yes | Mode collection token. |
| `membership` | object | yes | Collection membership fields to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "Forms": {},
      "Links": {},
      "memberId": "Ava Chen",
      "memberToken": "string",
      "memberType": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Member email address. |
| `Forms` | object | Mode HAL forms. |
| `Links` | object | Mode HAL links. |
| `memberId` | string | Mode member identifier. |
| `memberToken` | string | Mode member token. |
| `memberType` | string | Mode member type. |
| `token` | string | Mode collection membership token. |

## Native endpoint

Through the native Mode API, this operation is `POST /spaces/[:space]/memberships` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection-membership.md) for the provider-specific parameters and requirements.

