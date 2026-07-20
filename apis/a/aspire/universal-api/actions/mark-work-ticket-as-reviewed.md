# Aspire: Mark Work Ticket As Reviewed

Marks a work ticket as reviewed in your Aspire account.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/mark-work-ticket-as-reviewed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/mark-work-ticket-as-reviewed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workTicketId": 1,
  "reviewedDateTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/mark-work-ticket-as-reviewed', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workTicketId": 1,
    "reviewedDateTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workTicketId` | number | yes |  |
| `reviewedDateTime` | date | yes |  |
| `reviewedUserId` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `POST WorkTicketStatus/MarkWorkTicketAsReviewed` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-work-ticket-as-reviewed.md) for the provider-specific parameters and requirements.

