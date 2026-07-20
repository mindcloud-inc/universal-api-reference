# KleverKey: Update Access Group Partially



```
PUT https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/update-access-group-partially
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/update-access-group-partially" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "accessGroupId": 1,
  "op": "string",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/update-access-group-partially', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "accessGroupId": 1,
    "op": "string",
    "path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes |  |
| `accessGroupId` | number | yes |  |
| `op` | string | yes | JSON Patch operation. Use replace for /userIds or /lockIds updates. |
| `path` | string | yes | JSON Patch target path. Supported values from docs are /userIds and /lockIds. |
| `value[]` | array<number> | no | Replacement IDs for the target path. |

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

Through the native KleverKey API, this operation is `PATCH /api/v1/organizations/:organizationId/access-groups/:accessGroupId` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-access-group-partially.md) for the provider-specific parameters and requirements.

