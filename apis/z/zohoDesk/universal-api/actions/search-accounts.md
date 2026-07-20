# Zoho Desk: Search Accounts



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/search-accounts?${params}`, {
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
| `id` | string | no | Search for an exact Zoho Desk account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "website": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `createdTime` | date |  |
| `email` | string |  |
| `id` | string |  |
| `modifiedTime` | date |  |
| `phone` | string |  |
| `website` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /accounts/search` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-accounts.md) for the provider-specific parameters and requirements.

