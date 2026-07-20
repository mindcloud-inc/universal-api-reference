# Instatus: List Status Pages



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-status-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-status-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/list-status-pages?${params}`, {
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
      "customDomain": "string",
      "id": "string",
      "language": "string",
      "mainStatus": "string",
      "name": "Ava Chen",
      "private": true,
      "status": "string",
      "subdomain": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customDomain` | string |  |
| `id` | string |  |
| `language` | string |  |
| `mainStatus` | string |  |
| `name` | string |  |
| `private` | boolean |  |
| `status` | string |  |
| `subdomain` | string |  |
| `updatedAt` | date |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v2/pages` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-status-pages.md) for the provider-specific parameters and requirements.

