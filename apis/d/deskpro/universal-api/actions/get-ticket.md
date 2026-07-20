# Deskpro: Get Ticket

Retrieves a ticket record from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-ticket?${params}`, {
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
| `ticketId` | number | yes | The Deskpro ticket id to retrieve. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessCode": "string",
      "agent": 1,
      "agentTeam": 1,
      "auth": "string",
      "brand": 1,
      "countAgentReplies": 1,
      "countUserReplies": 1,
      "dateArchived": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateFirstAgentAssign": "2026-05-07T12:00:00.000Z",
      "dateFirstAgentReply": "2026-05-07T12:00:00.000Z",
      "dateLastAgentReply": "2026-05-07T12:00:00.000Z",
      "dateLastUserReply": "2026-05-07T12:00:00.000Z",
      "dateResolved": "2026-05-07T12:00:00.000Z",
      "dateStatus": "2026-05-07T12:00:00.000Z",
      "department": 1,
      "hasAttachments": true,
      "id": 1,
      "isHold": true,
      "organization": 1,
      "originalSubject": "string",
      "person": 1,
      "personEmail": "ava@example.com",
      "ref": "string",
      "status": "string",
      "subject": "string",
      "ticketStatus": "string",
      "urgency": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessCode` | string |  |
| `agent` | number |  |
| `agentTeam` | number |  |
| `auth` | string |  |
| `brand` | number |  |
| `countAgentReplies` | number |  |
| `countUserReplies` | number |  |
| `dateArchived` | date |  |
| `dateCreated` | date |  |
| `dateFirstAgentAssign` | date |  |
| `dateFirstAgentReply` | date |  |
| `dateLastAgentReply` | date |  |
| `dateLastUserReply` | date |  |
| `dateResolved` | date |  |
| `dateStatus` | date |  |
| `department` | number |  |
| `hasAttachments` | boolean |  |
| `id` | number |  |
| `isHold` | boolean |  |
| `organization` | number |  |
| `originalSubject` | string |  |
| `person` | number |  |
| `personEmail` | string |  |
| `ref` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `ticketStatus` | string |  |
| `urgency` | number |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /tickets/:ticketId` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

