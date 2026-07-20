# Deskpro: List Ticket Logs

Retrieves a list of ticket logs from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&ticketId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ticketId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-ticket-logs?${params}`, {
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
| `ticketId` | number | yes | The Deskpro ticket id whose logs to list. Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionType": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "details": {
        "creationSystem": "string",
        "emailFrom": "ava@example.com",
        "emailTo": [
          "ava@example.com"
        ],
        "event": "string",
        "eventMethod": "string",
        "eventPerformer": "string",
        "isAgentMessage": true,
        "isAgentNote": true,
        "messageId": "string",
        "new": "string",
        "newBrandId": 1,
        "newBrandName": "Ava Chen",
        "newDepartmentId": 1,
        "newDepartmentTitle": "string",
        "newPersonEmail": "ava@example.com",
        "newPersonId": 1,
        "newPersonName": "Ava Chen",
        "newSubject": "string",
        "old": "string",
        "oldSubject": "string",
        "personEmail": "ava@example.com",
        "personId": 1,
        "personName": "Ava Chen",
        "ticketId": "string"
      },
      "id": 1,
      "messageHtml": "string",
      "messageText": "string",
      "parent": 1,
      "person": 1,
      "ticket": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionType` | string |  |
| `dateCreated` | date |  |
| `details.creationSystem` | string |  |
| `details.emailFrom` | string |  |
| `details.emailTo[]` | string |  |
| `details.event` | string |  |
| `details.eventMethod` | string |  |
| `details.eventPerformer` | string |  |
| `details.isAgentMessage` | boolean |  |
| `details.isAgentNote` | boolean |  |
| `details.messageId` | string |  |
| `details.new` | string |  |
| `details.newBrandId` | number |  |
| `details.newBrandName` | string |  |
| `details.newDepartmentId` | number |  |
| `details.newDepartmentTitle` | string |  |
| `details.newPersonEmail` | string |  |
| `details.newPersonId` | number |  |
| `details.newPersonName` | string |  |
| `details.newSubject` | string |  |
| `details.old` | string |  |
| `details.oldSubject` | string |  |
| `details.personEmail` | string |  |
| `details.personId` | number |  |
| `details.personName` | string |  |
| `details.ticketId` | string |  |
| `id` | number |  |
| `messageHtml` | string |  |
| `messageText` | string |  |
| `parent` | number |  |
| `person` | number |  |
| `ticket` | number |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /tickets/:ticketId/logs` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ticket-logs.md) for the provider-specific parameters and requirements.

