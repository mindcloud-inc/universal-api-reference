# Harvestr.io: Create Message



```
POST https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "content": "string",
  "requester": {},
  "requester.type": "string",
  "requester.externalUid": "string",
  "requester.email": "ava@example.com",
  "requester.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "content": "string",
    "requester": {},
    "requester.type": "string",
    "requester.externalUid": "string",
    "requester.email": "ava@example.com",
    "requester.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Message title |
| `content` | string | yes | Message content |
| `requester` | object | yes | Requester to be upserted |
| `requester.type` | string | yes | Customer type (USER or COMPANY) |
| `requester.externalUid` | string | yes | External unique identifier for the customer |
| `requester.email` | string | yes | Email identifier (only for type: USER) |
| `requester.name` | string | yes | Customer name (always required) |
| `submitter` | object | no | Submitter to be upserted (optional) |
| `submitter.externalUid` | string | no | External unique identifier for the company |
| `submitter.email` | string | no | Company email |
| `submitter.name` | string | no | Company name (always required) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `integrationId` | string | no | Integration ID |
| `integrationUrl` | string | no | Integration URL |
| `channel` | string | no | Message channel |
| `labels[]` | array<string> | no | Message labels |

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

Through the native Harvestr.io API, this operation is `POST /message` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

