# Deskpro: List Ticket Approvals

Retrieves a list of ticket approvals from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-approvals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-approvals?connectionId=$CONNECTION_ID&limit=25&offset=0&ticketId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticketId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-approvals?${params}`, {
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
| `ticketId` | number | yes | The Deskpro ticket id whose approvals to list. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvers": [
        1
      ],
      "canApproversViewSubject": true,
      "cancelledAt": "2026-05-07T12:00:00.000Z",
      "cancelledBy": 1,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "lastApprovedResponseAt": "2026-05-07T12:00:00.000Z",
      "lastRejectResponseAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "requiredApprovals": 1,
      "requiredRejections": 1,
      "responses": [
        1
      ],
      "status": "string",
      "ticket": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvers[]` | number | Approver person IDs. |
| `canApproversViewSubject` | boolean | Whether approvers can view the ticket subject. |
| `cancelledAt` | date | When the approval was cancelled. |
| `cancelledBy` | number | The person who cancelled the approval. |
| `completedAt` | date | When the approval completed. |
| `createdAt` | date | When the approval was created. |
| `description` | string | The approval description. |
| `id` | number | The unique ID of the ticket approval. |
| `lastApprovedResponseAt` | date | When the last approval response was recorded. |
| `lastRejectResponseAt` | date | When the last rejection response was recorded. |
| `name` | string | The approval name. |
| `requiredApprovals` | number | Number of approvals required. |
| `requiredRejections` | number | Number of rejections required. |
| `responses[]` | number | Approval response IDs. |
| `status` | string | The approval status. |
| `ticket` | number | The related ticket ID. |
| `type` | number | Approval type ID. |

## Native endpoint

Through the native Deskpro API, this operation is `GET /tickets/:ticketId/ticket_approvals` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-approvals.md) for the provider-specific parameters and requirements.

