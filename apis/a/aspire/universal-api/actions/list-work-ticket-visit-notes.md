# Aspire: List Work Ticket Visit Notes

Retrieves work ticket visit notes from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-visit-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-visit-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-visit-notes?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedByUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "EndDateTime": "2026-05-07T12:00:00.000Z",
      "IsPublic": true,
      "LastModifiedByUserID": 1,
      "LastModifiedByUserName": "Ava Chen",
      "LastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "Note": "string",
      "RouteID": 1,
      "RouteName": "Ava Chen",
      "ScheduledDate": "2026-05-07T12:00:00.000Z",
      "StartDateTime": "2026-05-07T12:00:00.000Z",
      "WorkTicketID": 1,
      "WorkTicketNumber": 1,
      "WorkTicketVisitID": 1,
      "WorkTicketVisitNoteID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedByUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `EndDateTime` | date |  |
| `IsPublic` | boolean |  |
| `LastModifiedByUserID` | number |  |
| `LastModifiedByUserName` | string |  |
| `LastModifiedDateTime` | date |  |
| `Note` | string |  |
| `RouteID` | number |  |
| `RouteName` | string |  |
| `ScheduledDate` | date |  |
| `StartDateTime` | date |  |
| `WorkTicketID` | number |  |
| `WorkTicketNumber` | number |  |
| `WorkTicketVisitID` | number |  |
| `WorkTicketVisitNoteID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkTicketVisitNotes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-ticket-visit-notes.md) for the provider-specific parameters and requirements.

