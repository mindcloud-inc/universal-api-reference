# Zoho Desk: List Tickets

List Tickets with optional filters

```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-tickets?${params}`, {
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
| `status` | string | no | Filter by resolution status of the ticket. You can specify multiple status values here. Accepts multiple values as an array. |
| `channel` | list<string> | no | Filter by Channel through which the tickets originated. You can specify multiple channels. Accepts multiple values as an array. |
| `priority` | string | no | Filter tickets by Priority. Accepts multiple values as an array. |
| `receivedInDays` | list<number> | no | Fetches recent tickets based on `Customer Response Time`. |
| `assignee` | list<string> | no | Filter tickets by assignee. Allowed Values: - `Unassiged` - 1 or more valid `assigneeIds` One of: `Unassigned`. Accepts multiple values as an array. |
| `departmentIds` | list<number> | no | Select the department(s) from which the tickets need to be queried. Accepts multiple values as an array. |
| `teamIds` | string | no | Filter Tickets by Teams. Allowed Values: - `Unassigned` - 1 or more valid `teamId` Accepts multiple values as an array. |
| `viewIds` | number | no | ID of the View to apply while fetching the resources. |
| `include` | list<string> | no | Specify any additional information you'd like to retrieve related to the tickets. Accepts multiple values as an array. |
| `fields` | string | no | Specify fields in your portal that you want to retrieve. (both pre-defined and custom fields are allowed) Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "channel": "string",
      "contactId": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "departmentId": "string",
      "id": "string",
      "isArchived": true,
      "isSpam": true,
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "statusType": "string",
      "subject": "string",
      "ticketNumber": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `channel` | string |  |
| `contactId` | string |  |
| `createdTime` | date |  |
| `departmentId` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isSpam` | boolean |  |
| `modifiedTime` | date |  |
| `status` | string |  |
| `statusType` | string |  |
| `subject` | string |  |
| `ticketNumber` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /tickets` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

