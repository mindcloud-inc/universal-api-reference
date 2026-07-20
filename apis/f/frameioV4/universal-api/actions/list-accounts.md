# Frame.io v4: List Accounts

Retrieves accounts from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": "string",
      "image": "string",
      "mountedStorageEnabled": true,
      "roles": [
        [
          "string"
        ]
      ],
      "storageLimit": 1,
      "storageUsage": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "v4MigratedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Created Timestamp |
| `displayName` | string | Account Name |
| `id` | string | Account ID |
| `image` | string | The account image url |
| `mountedStorageEnabled` | boolean | Whether mounted storage is enabled for this account |
| `roles[]` | array<string> | Account User Roles |
| `storageLimit` | number | The number of bytes of non-archived storage in the account. Value is nil when there is no limit |
| `storageUsage` | number | The number of bytes of non-archived storage the account is using |
| `updatedAt` | date | Update timestamp |
| `v4MigratedAt` | date | Migration timestamp |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

