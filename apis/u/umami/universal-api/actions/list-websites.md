# Umami: List Websites



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-websites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-websites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-websites?${params}`, {
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
| `includeTeams` | boolean | no | Include websites where you are the team owner. |
| `search` | string | no | Search text used to filter websites. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "resetAt": "2026-05-07T12:00:00.000Z",
      "shareId": "string",
      "teamId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `createdBy` | string | User who created the website. |
| `deletedAt` | date | Deletion timestamp, if soft-deleted. |
| `domain` | string | Tracked domain. |
| `id` | string | Website ID. |
| `name` | string | Website name. |
| `resetAt` | date | Timestamp of the last reset, if any. |
| `shareId` | string | Share identifier when public sharing is enabled. |
| `teamId` | string | Owning team ID, if any. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Owner user ID. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-websites.md) for the provider-specific parameters and requirements.

