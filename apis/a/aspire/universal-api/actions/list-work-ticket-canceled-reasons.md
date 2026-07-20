# Aspire: List Work Ticket Canceled Reasons

Retrieves work ticket canceled reasons from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-canceled-reasons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-canceled-reasons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-canceled-reasons?${params}`, {
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
      "Active": true,
      "CreatedByUserId": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "LastModifiedByUserId": 1,
      "LastModifiedByUserName": "Ava Chen",
      "LastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "WorkTicketCanceledReasonId": 1,
      "WorkTicketCanceledReasonName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `CreatedByUserId` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `LastModifiedByUserId` | number |  |
| `LastModifiedByUserName` | string |  |
| `LastModifiedDateTime` | date |  |
| `WorkTicketCanceledReasonId` | number |  |
| `WorkTicketCanceledReasonName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkTicketCanceledReasons` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-ticket-canceled-reasons.md) for the provider-specific parameters and requirements.

