# Atera: Find modified tickets

Finds recently modified tickets in Atera.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-modified-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-modified-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-modified-tickets?${params}`, {
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
| `date` | string | no | Return tickets modified since this UTC timestamp. Example: `2026-03-16T00:00:00Z`. |
| `includeComments` | boolean | no | Include the ticket's last comments. |
| `includeRelations` | boolean | no | Include ticket relation information. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "EndUserEmail": "ava@example.com",
      "EndUserFirstName": "Ava",
      "EndUserID": 1,
      "EndUserLastName": "Chen",
      "EndUserPhone": "string",
      "OffSiteDurationMinutes": 1,
      "OffSiteDurationSeconds": 1,
      "OffSLADurationMinutes": 1,
      "OnSiteDurationMinutes": 1,
      "OnSiteDurationSeconds": 1,
      "OnSLADurationMinutes": 1,
      "RelationType": "string",
      "TechnicianContactID": 1,
      "TechnicianEmail": "ava@example.com",
      "TechnicianFirstCommentDate": "string",
      "TechnicianFullName": "Ava Chen",
      "TicketCreatedDate": "string",
      "TicketID": 1,
      "TicketImpact": "string",
      "TicketNumber": "string",
      "TicketPriority": "string",
      "TicketSource": "string",
      "TicketStatus": "string",
      "TicketTitle": "string",
      "TicketType": "string",
      "TotalDurationMinutes": 1,
      "TotalDurationSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerID` | number |  |
| `CustomerName` | string |  |
| `EndUserEmail` | string |  |
| `EndUserFirstName` | string |  |
| `EndUserID` | number |  |
| `EndUserLastName` | string |  |
| `EndUserPhone` | string |  |
| `OffSiteDurationMinutes` | number |  |
| `OffSiteDurationSeconds` | number |  |
| `OffSLADurationMinutes` | number |  |
| `OnSiteDurationMinutes` | number |  |
| `OnSiteDurationSeconds` | number |  |
| `OnSLADurationMinutes` | number |  |
| `RelationType` | string |  |
| `TechnicianContactID` | number |  |
| `TechnicianEmail` | string |  |
| `TechnicianFirstCommentDate` | string |  |
| `TechnicianFullName` | string |  |
| `TicketCreatedDate` | string |  |
| `TicketID` | number |  |
| `TicketImpact` | string |  |
| `TicketNumber` | string |  |
| `TicketPriority` | string |  |
| `TicketSource` | string |  |
| `TicketStatus` | string |  |
| `TicketTitle` | string |  |
| `TicketType` | string |  |
| `TotalDurationMinutes` | number |  |
| `TotalDurationSeconds` | number |  |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/tickets/lastmodified` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-modified-tickets.md) for the provider-specific parameters and requirements.

