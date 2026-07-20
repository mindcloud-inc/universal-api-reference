# Crisp: List Conversations

Retrieves conversations from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-conversations?connectionId=$CONNECTION_ID&limit=25&offset=0&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-conversations?${params}`, {
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
| `websiteId` | string | yes | The website identifier. |
| `pageNumber` | number | no | Page number for conversations paging. Default: `1`. |
| `perPage` | number | no | Page size for conversations paging (between 20 and 50, defaults to 20). Default: `20`. |
| `searchQuery` | string | no | Search query in conversations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": {},
      "assigned": {},
      "availability": "string",
      "inboxId": "string",
      "isBlocked": true,
      "isVerified": true,
      "meta": {},
      "peopleId": "string",
      "sessionId": "string",
      "state": "string",
      "status": 1,
      "unread": {},
      "websiteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | object |  |
| `assigned` | object |  |
| `availability` | string |  |
| `inboxId` | string |  |
| `isBlocked` | boolean |  |
| `isVerified` | boolean |  |
| `meta` | object |  |
| `peopleId` | string |  |
| `sessionId` | string |  |
| `state` | string |  |
| `status` | number |  |
| `unread` | object |  |
| `websiteId` | string |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/conversations/:page_number` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

