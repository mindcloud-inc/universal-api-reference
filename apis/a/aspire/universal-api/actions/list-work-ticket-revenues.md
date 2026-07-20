# Aspire: List Work Ticket Revenues

Total income generated within a work ticket.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-revenues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-revenues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-revenues?${params}`, {
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
      "accountingPeriodID": {},
      "createdDateTime": "string",
      "editedByUserID": {},
      "editedByUserName": {},
      "editedDateTime": {},
      "revenueAmount": 1,
      "revenueMonth": "string",
      "workTicketID": 1,
      "workTicketNumber": 1,
      "workTicketRevenueID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingPeriodID` | object |  |
| `createdDateTime` | string |  |
| `editedByUserID` | object |  |
| `editedByUserName` | object |  |
| `editedDateTime` | object |  |
| `revenueAmount` | number |  |
| `revenueMonth` | string |  |
| `workTicketID` | number |  |
| `workTicketNumber` | number |  |
| `workTicketRevenueID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkTicketRevenues` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-ticket-revenues.md) for the provider-specific parameters and requirements.

