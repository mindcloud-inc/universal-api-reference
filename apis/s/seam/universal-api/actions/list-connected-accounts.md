# Seam: List Connected Accounts

Retrieves a list of connected accounts from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-connected-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-connected-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-connected-accounts?${params}`, {
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
      "acceptedCapabilities": [
        "string"
      ],
      "accountType": "string",
      "accountTypeDisplayName": "Ava Chen",
      "automaticallyManageNewDevices": true,
      "connectedAccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "displayName": "Ava Chen",
      "errors": [
        {}
      ],
      "imageUrl": "https://example.com",
      "userIdentifier": {},
      "warnings": [
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
| `acceptedCapabilities` | array<string> |  |
| `accountType` | string |  |
| `accountTypeDisplayName` | string |  |
| `automaticallyManageNewDevices` | boolean |  |
| `connectedAccountId` | string |  |
| `createdAt` | date |  |
| `customMetadata` | object |  |
| `displayName` | string |  |
| `errors` | array<object> |  |
| `imageUrl` | string |  |
| `userIdentifier` | object |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Seam API, this operation is `POST /connected_accounts/list` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-connected-accounts.md) for the provider-specific parameters and requirements.

