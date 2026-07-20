# Scanova: Update User Role



```
PUT https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-user-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-user-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sharedUserId": 1,
  "accessLevel": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-user-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sharedUserId": 1,
    "accessLevel": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sharedUserId` | number | yes | ID of the shared user |
| `accessLevel` | list | yes | New access level ID for the user. Pre-defined access levels: Manager (1), Admin (2), Viewer (3) One of: `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_level": {},
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "invitation_accepted_on": "2026-05-07T12:00:00.000Z",
      "invitation_sent_on": "2026-05-07T12:00:00.000Z",
      "is_invitation_accepted": true,
      "is_invitation_sent": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "shared_user": {},
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_level` | object |  |
| `created` | date |  |
| `id` | number |  |
| `invitation_accepted_on` | date |  |
| `invitation_sent_on` | date |  |
| `is_invitation_accepted` | boolean |  |
| `is_invitation_sent` | boolean |  |
| `modified` | date |  |
| `shared_user` | object |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Scanova API, this operation is `PATCH /multi-users/{shared-user-id}/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-role.md) for the provider-specific parameters and requirements.

