# Rownd Data Privacy: Insert or Update User Profile Data



```
POST https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/insert-or-update-user-profile-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/insert-or-update-user-profile-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/insert-or-update-user-profile-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | yes | Rownd user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "auth_level": "string",
      "connection_map": {},
      "data": {},
      "groups": [
        {}
      ],
      "meta": {},
      "rownd_user": "string",
      "state": "string",
      "verified_data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | User attributes. |
| `auth_level` | string | User authentication level. |
| `connection_map` | object | Connection mapping details. |
| `data` | object | Primary user profile fields. |
| `groups` | array<object> | Groups the user belongs to. |
| `meta` | object | User activity metadata. |
| `rownd_user` | string | Rownd user identifier. |
| `state` | string | User state. |
| `verified_data` | object | Verified user profile fields. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `PUT /users/:user/data` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-or-update-user-profile-data.md) for the provider-specific parameters and requirements.

