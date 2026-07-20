# Jodoo: Update Member



```
PUT https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "jodoo_member_001",
  "name": "Wizard Sandbox Updated",
  "departments[]": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "jodoo_member_001",
    "name": "Wizard Sandbox Updated",
    "departments[]": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Username of the member to update. Jodoo only allows letters, digits, and underscores. Example: `jodoo_member_001`. |
| `name` | string | yes | Updated display name for the member. Example: `Wizard Sandbox Updated`. |
| `departments[]` | array<number> | yes | Array of department numbers for the member. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departments": [
        1
      ],
      "name": "Ava Chen",
      "status": 1,
      "type": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departments[]` | number |  |
| `name` | string |  |
| `status` | number |  |
| `type` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /corp/user/update` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

