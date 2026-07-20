# KleverKey: Revoke Permission



```
DELETE https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/revoke-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/revoke-permission?connectionId=$CONNECTION_ID&organizationId=1&lockId=1&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1",
  "lockId": "1",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/revoke-permission?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes |  |
| `lockId` | number | yes |  |
| `userId` | number | yes |  |

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

Through the native KleverKey API, this operation is `DELETE /api/v1/organizations/:organizationId/permissions/:lockId/:userId` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-permission.md) for the provider-specific parameters and requirements.

