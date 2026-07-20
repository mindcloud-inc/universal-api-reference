# Syncro: List Ticket Comments

Retrieves comments for a ticket from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-ticket-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-ticket-comments?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-ticket-comments?${params}`, {
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
| `id` | number | yes | The Syncro ticket ID. |
| `page` | number | no |  |
| `perPage` | number | no |  |
| `commentFormat` | string | no |  |
| `sortBy` | string | no |  |
| `sortDirection` | string | no |  |
| `createdAfter` | date | no |  |
| `createdBefore` | date | no |  |
| `updatedAfter` | date | no |  |
| `updatedBefore` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {
          "body": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "hidden": true,
          "id": 1,
          "isRichText": true,
          "subject": "string",
          "tech": "string",
          "ticketId": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userId": 1
        }
      ],
      "meta": {
        "page": 1,
        "perPage": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments[].body` | string |  |
| `comments[].createdAt` | date |  |
| `comments[].hidden` | boolean |  |
| `comments[].id` | number |  |
| `comments[].isRichText` | boolean |  |
| `comments[].subject` | string |  |
| `comments[].tech` | string |  |
| `comments[].ticketId` | number |  |
| `comments[].updatedAt` | date |  |
| `comments[].userId` | number |  |
| `meta.page` | number |  |
| `meta.perPage` | number |  |
| `meta.totalPages` | number |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /tickets/:id/comments` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-comments.md) for the provider-specific parameters and requirements.

