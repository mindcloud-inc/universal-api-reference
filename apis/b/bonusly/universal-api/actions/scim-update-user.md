# Bonusly: SCIM Update User

Updates an existing SCIM user in Bonusly.

```
PUT https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/scim-update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/scim-update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "userName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/scim-update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "userName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The SCIM user ID. |
| `userName` | string | yes | SCIM username for the user resource. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "meta": {},
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | string |  |
| `meta` | object |  |
| `userName` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `PUT https://bonus.ly/api/scim11/Users/:id` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scim-update-user.md) for the provider-specific parameters and requirements.

