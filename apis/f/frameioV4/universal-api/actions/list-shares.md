# Frame.io v4: List Shares

Retrieves shares for a project in Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-shares
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-shares?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/list-shares?${params}`, {
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
| `accountId` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "collectionId": "string",
      "commentingEnabled": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "downloadingEnabled": true,
      "enabled": true,
      "expiration": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastViewedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "passphrase": "string",
      "shortUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `collectionId` | string | Collection ID |
| `commentingEnabled` | boolean |  |
| `createdAt` | date | Creation timestamp |
| `description` | string | Share description |
| `downloadingEnabled` | boolean |  |
| `enabled` | boolean |  |
| `expiration` | date | Expiration timestamp |
| `id` | string | Share ID |
| `lastViewedAt` | date | Last viewed timestamp |
| `name` | string | Share name |
| `passphrase` | string | Passphrase to access share, if passphrase is required and not given it will be generated |
| `shortUrl` | string | Share URL |
| `updatedAt` | date | Update timestamp |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/projects/:projectId/shares` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shares.md) for the provider-specific parameters and requirements.

