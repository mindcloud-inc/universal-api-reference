# Google Mail: List Emails

Retrieves messages from a Gmail mailbox.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-emails?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-emails?${params}`, {
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
| `q` | string | no | Search threads matching a query. Supports the same query format as the Gmail search box. For example: "from:myusername@example.com is:unread". |
| `labelIds` | list<string> | no | Only return messages with labels that match all of the specified label IDs. Messages in a thread might have labels that other messages in the same thread don't have. |
| `receivedAfter` | date | no | Filters emails to only include those received after a specified date and time |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /messages` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-emails.md) for the provider-specific parameters and requirements.

