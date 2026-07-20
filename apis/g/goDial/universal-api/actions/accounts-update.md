# GoDial: Update User

Updates an existing user in GoDial.

```
PUT https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "role": "string",
  "teamsId[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "role": "string",
    "teamsId[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Account ID. |
| `role` | string | yes | Provide role of the User. Accepted values: teammanager, submanager, agent |
| `teamsId[]` | array<string> | yes | Provide teamsId for the User as a JSON array, e.g. ["teamId1"] |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "role": "string",
      "teamsId": [
        "string"
      ],
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `role` | string |  |
| `teamsId` | array<string> |  |
| `username` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `PUT /externals/accounts/[:id]/update` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accounts-update.md) for the provider-specific parameters and requirements.

