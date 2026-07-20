# KleverKey: Grant Permission



```
POST https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/grant-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/grant-permission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "lockId": 1,
  "userId": 1,
  "permissionType": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/grant-permission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "lockId": 1,
    "userId": 1,
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
| `lockId` | number | yes |  |
| `userId` | number | yes |  |
| `permissionType` | number | yes | 1 = Always, 2 = TimeProfile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateGranted": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": 1,
      "isNotificationEnabled": true,
      "isSynced": true,
      "lock": {},
      "lockName": "Ava Chen",
      "permissionStatus": 1,
      "permissionTypeSet": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `dateGranted` | date |  |
| `dateUpdated` | date |  |
| `displayName` | string |  |
| `id` | number |  |
| `isNotificationEnabled` | boolean |  |
| `isSynced` | boolean |  |
| `lock` | object |  |
| `lockName` | string |  |
| `permissionStatus` | number |  |
| `permissionTypeSet` | number |  |
| `user` | object |  |

## Native endpoint

Through the native KleverKey API, this operation is `PUT /api/v1/organizations/:organizationId/permissions/:lockId/:userId` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/grant-permission.md) for the provider-specific parameters and requirements.

