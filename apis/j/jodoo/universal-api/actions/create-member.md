# Jodoo: Create Member



```
POST https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "jodoo_member_001",
  "name": "Wizard Sandbox",
  "departments[]": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "jodoo_member_001",
    "name": "Wizard Sandbox",
    "departments[]": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Username for the new member. Jodoo only allows letters, digits, and underscores. Example: `jodoo_member_001`. |
| `name` | string | yes | Display name for the new member. Example: `Wizard Sandbox`. |
| `departments[]` | array<number> | yes | Array of department numbers for the new member. Example: `1`. |

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

Through the native Jodoo API, this operation is `POST /corp/user/create` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

