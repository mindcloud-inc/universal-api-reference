# HelpDesk: Get Ticket

Retrieves a ticket from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-ticket?${params}`, {
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
| `ticketID` | string | yes | Unique HelpDesk ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignment": {
        "team": {
          "ID": "string",
          "name": "Ava Chen"
        }
      },
      "cc": [
        {}
      ],
      "childTickets": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "detectedLanguage": "string",
      "events": [
        {}
      ],
      "followers": [
        "string"
      ],
      "ID": "string",
      "integrations": {},
      "lastMessageAt": "2026-05-07T12:00:00.000Z",
      "licenseID": 1,
      "priority": 1,
      "ratingRequestSent": true,
      "requester": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "shortID": "string",
      "source": {
        "detailedSource": "string",
        "type": "string"
      },
      "spam": {
        "status": true
      },
      "status": "string",
      "subject": "string",
      "tagIDs": [
        "string"
      ],
      "teamIDs": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignment` | object |  |
| `assignment.team` | object |  |
| `assignment.team.ID` | string |  |
| `assignment.team.name` | string |  |
| `cc` | array<object> |  |
| `childTickets` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `detectedLanguage` | string |  |
| `events` | array<object> |  |
| `followers` | array<string> |  |
| `ID` | string |  |
| `integrations` | object |  |
| `lastMessageAt` | date |  |
| `licenseID` | number |  |
| `priority` | number |  |
| `ratingRequestSent` | boolean |  |
| `requester` | object |  |
| `requester.email` | string |  |
| `requester.name` | string |  |
| `shortID` | string |  |
| `source` | object |  |
| `source.detailedSource` | string |  |
| `source.type` | string |  |
| `spam` | object |  |
| `spam.status` | boolean |  |
| `status` | string |  |
| `subject` | string |  |
| `tagIDs` | array<string> |  |
| `teamIDs` | array<string> |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/tickets/:ticketID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

