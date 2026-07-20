# Harvestr.io: List Messages



```
GET https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-messages?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBefore` | date | no | Filter items created before this date (ISO 8601 format) |
| `createdAfter` | date | no | Filter items created after this date (ISO 8601 format) |
| `updatedBefore` | date | no | Filter items updated before this date (ISO 8601 format) |
| `updatedAfter` | date | no | Filter items updated after this date (ISO 8601 format) |
| `channel` | string | no | Filter messages by channel |
| `requesterId` | string | no | Filter messages by requester ID |
| `hasFeedback` | boolean | no | Filter messages by whether they have feedback linked or not |
| `customInboxId` | string | no | Filter messages by custom inbox ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assigneeId": "string",
      "bin": true,
      "channel": "string",
      "clientId": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "integrationId": "string",
      "integrationUrl": "https://example.com",
      "labels": [
        "string"
      ],
      "read": true,
      "receivedAt": "2026-05-07T12:00:00.000Z",
      "requesterId": "string",
      "submitterId": "string",
      "title": "string",
      "updated": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the message is archived |
| `assigneeId` | string | Identifier of the assignee |
| `bin` | boolean | Whether the message is in the bin |
| `channel` | string | Channel through which the message was received |
| `clientId` | string | Client identifier |
| `content` | string | Content of the message |
| `createdAt` | date | Creation date of the message |
| `id` | string | Unique identifier of the message |
| `integrationId` | string | When you import messages from an external source (e.g.: Intercom) into Harvestr, this is the message ID in the source tool |
| `integrationUrl` | string | When you import messages from an external source (e.g.: Intercom) into Harvestr, this is the URL of the message in the source tool |
| `labels` | array<string> | Labels associated with this message |
| `read` | boolean | Whether the message has been read |
| `receivedAt` | date | Date when the message was received |
| `requesterId` | string | Identifier of the requester |
| `submitterId` | string | Identifier of the submitter |
| `title` | string | Title of the message |
| `updated` | boolean | Whether the message has been updated |
| `updatedAt` | date | Last update date of the message |

## Native endpoint

Through the native Harvestr.io API, this operation is `GET /message` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

