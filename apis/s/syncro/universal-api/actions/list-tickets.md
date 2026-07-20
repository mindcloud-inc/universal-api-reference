# Syncro: List Tickets

Retrieves a list of tickets from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-tickets?${params}`, {
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
| `customerId` | number | no |  |
| `contactId` | number | no |  |
| `number` | string | no |  |
| `resolvedAfter` | date | no |  |
| `createdAfter` | date | no |  |
| `sinceUpdatedAt` | date | no |  |
| `status` | string | no |  |
| `query` | string | no |  |
| `userId` | number | no |  |
| `mine` | boolean | no |  |
| `ticketSearchId` | number | no |  |
| `page` | number | no |  |
| `commentFormat` | string | no |  |
| `allComments` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "page": 1,
        "totalPages": 1
      },
      "tickets": [
        {
          "billingStatus": "string",
          "comments": [
            {
              "body": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "id": 1,
              "subject": "string"
            }
          ],
          "contactId": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerBusinessThenName": "Ava Chen",
          "customerId": 1,
          "dueDate": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "number": 1,
          "priority": "string",
          "problemType": "string",
          "status": "string",
          "subject": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.page` | number |  |
| `meta.totalPages` | number |  |
| `tickets[].billingStatus` | string |  |
| `tickets[].comments[].body` | string |  |
| `tickets[].comments[].createdAt` | date |  |
| `tickets[].comments[].id` | number |  |
| `tickets[].comments[].subject` | string |  |
| `tickets[].contactId` | number |  |
| `tickets[].createdAt` | date |  |
| `tickets[].customerBusinessThenName` | string |  |
| `tickets[].customerId` | number |  |
| `tickets[].dueDate` | date |  |
| `tickets[].id` | number |  |
| `tickets[].number` | number |  |
| `tickets[].priority` | string |  |
| `tickets[].problemType` | string |  |
| `tickets[].status` | string |  |
| `tickets[].subject` | string |  |
| `tickets[].updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /tickets` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

