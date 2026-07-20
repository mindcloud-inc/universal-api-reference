# Atera: Find ticket comments

Finds comments for a specific Atera ticket.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-ticket-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-ticket-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&ticketId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticketId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-ticket-comments?${params}`, {
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
| `ticketId` | number | yes | System ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Comment": "string",
      "CommentHtml": "string",
      "Date": "string",
      "Email": "ava@example.com",
      "EndUserID": 1,
      "FirstName": "Ava",
      "IsInternal": true,
      "LastName": "Chen",
      "TechnicianContactID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Comment` | string |  |
| `CommentHtml` | string |  |
| `Date` | string |  |
| `Email` | string |  |
| `EndUserID` | number |  |
| `FirstName` | string |  |
| `IsInternal` | boolean |  |
| `LastName` | string |  |
| `TechnicianContactID` | number |  |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/tickets/:ticketId/comments` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-ticket-comments.md) for the provider-specific parameters and requirements.

