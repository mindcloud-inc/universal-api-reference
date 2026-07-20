# Cryptlex: List Licenses

Retrieves licenses from Cryptlex.

```
GET https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-licenses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-licenses?${params}`, {
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
| `page` | number | no | Page number. |
| `limit` | number | no | Number of records per page (1-100). |
| `sort` | string | no | Sort expression such as -createdAt. |
| `search` | string | no | Search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActivations": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "key": "string",
      "productId": "string",
      "revoked": true,
      "suspended": true,
      "totalActivations": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userLocked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActivations` | number |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `key` | string |  |
| `productId` | string |  |
| `revoked` | boolean |  |
| `suspended` | boolean |  |
| `totalActivations` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userLocked` | boolean |  |

## Native endpoint

Through the native Cryptlex API, this operation is `GET /v3/licenses` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-licenses.md) for the provider-specific parameters and requirements.

