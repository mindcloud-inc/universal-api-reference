# Umami: Update Website



```
PUT https://connect.mindcloud.co/v1/universal/umami/latest/actions/update-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/umami/latest/actions/update-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string",
  "name": "Ava Chen",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umami/latest/actions/update-website', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string",
    "name": "Ava Chen",
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteId` | string | yes | The website ID. |
| `name` | string | yes | The website name in Umami. |
| `domain` | string | yes | The full tracked domain. |
| `shareId` | string | no | A share URL identifier. Set null to unshare. |

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
| `createdAt` | date | Website creation timestamp. |
| `createdBy` | string | User who created the website. |
| `deletedAt` | date | Deletion timestamp when soft-deleted. |
| `domain` | string | Tracked domain. |
| `id` | string | Website identifier. |
| `name` | string | Website name. |
| `replayConfig` | object | Replay configuration object when present. |
| `replayEnabled` | boolean | Whether replay is enabled. |
| `resetAt` | date | Timestamp when stats were last reset. |
| `shareId` | string | Public share identifier when enabled. |
| `teamId` | string | Owning team identifier when present. |
| `updatedAt` | date | Website update timestamp. |
| `userId` | string | Owning user identifier. |

## Native endpoint

Through the native Umami API, this operation is `POST /websites/:websiteId` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-website.md) for the provider-specific parameters and requirements.

