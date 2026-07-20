# Google Mail: Get Thread

Retrieves a Gmail thread.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-thread?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-thread?${params}`, {
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
| `id` | string | yes | (Required) The ID of the thread to retrieve. |
| `fields` | string | no | e.g. historyId,messages(id,labelIds,internalDate,snippet,payload/headers) |
| `format` | list<string> | no |  |
| `metadataHeaders` | string | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "historyId": "string",
      "labelIds": [
        "string"
      ],
      "messageLink": "https://example.com",
      "originalHeaders": [
        {
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "simpleHeaders": {
        "recipients": [
          {
            "email": "ava@example.com",
            "name": "Ava Chen"
          }
        ],
        "sender": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "subject": "string",
        "threadTopic": "string"
      },
      "snippet": "string",
      "subject": "string",
      "textContent": "string",
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `emailId` | string |  |
| `historyId` | string |  |
| `labelIds[]` | string |  |
| `messageLink` | string |  |
| `originalHeaders[].name` | string |  |
| `originalHeaders[].value` | string |  |
| `simpleHeaders.recipients[].email` | string |  |
| `simpleHeaders.recipients[].name` | string |  |
| `simpleHeaders.sender.email` | string |  |
| `simpleHeaders.sender.name` | string |  |
| `simpleHeaders.subject` | string |  |
| `simpleHeaders.threadTopic` | undefined |  |
| `snippet` | string |  |
| `subject` | string |  |
| `textContent` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /threads/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread.md) for the provider-specific parameters and requirements.

