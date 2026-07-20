# Umami: Get Website



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website?connectionId=$CONNECTION_ID&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website?${params}`, {
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
| `websiteId` | string | yes | The website ID. |

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
      "replayConfig": {},
      "replayEnabled": true,
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
| `replayConfig` | object | Replay configuration when enabled. |
| `replayEnabled` | boolean | Whether replay is enabled. |
| `resetAt` | date | Timestamp of the last reset, if any. |
| `shareId` | string | Share identifier when public sharing is enabled. |
| `teamId` | string | Owning team ID, if any. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Owner user ID. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website.md) for the provider-specific parameters and requirements.

