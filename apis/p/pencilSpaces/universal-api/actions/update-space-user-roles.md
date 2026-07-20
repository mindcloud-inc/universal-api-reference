# Pencil Spaces: Update Space User Roles



```
PUT https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-space-user-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-space-user-roles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-space-user-roles', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modifyUsers[]` | array<object> | no | Users whose role should be changed. |
| `modifyUsers[].role` | string | no | The new role for the user. |
| `modifyUsers[].userId` | string | no | The user whose Space role should change. |
| `notifyInvitees` | boolean | no | Whether Pencil should notify changed users. |
| `spaceId` | string | yes | The Space whose membership you want to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "customAttributes": [
        "string"
      ],
      "externalId": "string",
      "hosts": [
        {}
      ],
      "link": "https://example.com",
      "ownerId": "string",
      "participants": [
        {}
      ],
      "settings": {},
      "spaceId": "string",
      "title": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `customAttributes` | array<string> |  |
| `externalId` | string |  |
| `hosts` | array<object> |  |
| `link` | string |  |
| `ownerId` | string |  |
| `participants` | array<object> |  |
| `settings` | object |  |
| `spaceId` | string |  |
| `title` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Pencil Spaces API, this operation is `PATCH /spaces/:spaceId/updateUsers` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space-user-roles.md) for the provider-specific parameters and requirements.

