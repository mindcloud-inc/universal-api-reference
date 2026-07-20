# Teachlr Organizations: Invite User With Role



```
POST https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/invite-user-with-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/invite-user-with-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "role": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/invite-user-with-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "role": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the user to invite to the Teachlr school. |
| `role` | number | yes | Role to assign to the invited user. Teachlr accepts integer values from 2 to 4. Default: `4`. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address of the invited user. |
| `id` | number | Teachlr identifier of the invited user. |
| `username` | string | Teachlr username created for the invited user. |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `POST /invite` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user-with-role.md) for the provider-specific parameters and requirements.

