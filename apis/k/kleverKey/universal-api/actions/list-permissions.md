# KleverKey: List Permissions



```
GET https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/list-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/list-permissions?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/list-permissions?${params}`, {
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
| `organizationId` | number | yes | Organization ID |

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

Through the native KleverKey API, this operation is `GET /api/v1/organizations/:organizationId/permissions` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-permissions.md) for the provider-specific parameters and requirements.

