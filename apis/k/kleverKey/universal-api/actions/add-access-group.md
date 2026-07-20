# KleverKey: Add Access Group



```
POST https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-access-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-access-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "name": "Ava Chen",
  "lockIds[]": [
    1
  ],
  "userIds[]": [
    1
  ],
  "permissionType": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-access-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "name": "Ava Chen",
    "lockIds[]": [1],
    "userIds[]": [1],
    "permissionType": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes |  |
| `name` | string | yes |  |
| `lockIds[]` | array<number> | yes |  |
| `userIds[]` | array<number> | yes |  |
| `permissionType` | number | yes | 1 = Always, 2 = TimeProfile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "locks": [
        {}
      ],
      "name": "Ava Chen",
      "organizationId": 1,
      "permissionType": 1,
      "users": [
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
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `id` | number |  |
| `locks` | array<object> |  |
| `name` | string |  |
| `organizationId` | number |  |
| `permissionType` | number |  |
| `users` | array<object> |  |

## Native endpoint

Through the native KleverKey API, this operation is `POST /api/v1/organizations/:organizationId/access-groups` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-access-group.md) for the provider-specific parameters and requirements.

