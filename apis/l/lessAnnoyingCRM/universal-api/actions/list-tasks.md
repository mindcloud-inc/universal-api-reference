# Less Annoying CRM: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-tasks?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-tasks?${params}`, {
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
| `startDate` | date | yes | Lower bound of dates to fetch. |
| `endDate` | date | yes | Upper bound of dates to fetch. |
| `userFilter` | string | no | JSON array of UserIds to filter assignees. |
| `contactId` | string | no | Only return tasks attached to this contact. |
| `completionStatus` | string | no | Both, Incomplete, or Complete. |
| `sortDirection` | string | no | Ascending or Descending sort order. |
| `maxNumberOfResults` | number | no | Maximum number of results to return. |
| `page` | number | no | Pagination page number starting at 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "assignedToMetaData": {
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "calendarId": "string",
      "contactId": "string",
      "contactMetaData": {
        "assignedTo": "string",
        "name": "Ava Chen"
      },
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "isCompleted": true,
      "name": "Ava Chen",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `assignedToMetaData.firstName` | string |  |
| `assignedToMetaData.lastName` | string |  |
| `calendarId` | string |  |
| `contactId` | string |  |
| `contactMetaData.assignedTo` | string |  |
| `contactMetaData.name` | string |  |
| `dateCreated` | date |  |
| `description` | string |  |
| `dueDate` | date |  |
| `isCompleted` | boolean |  |
| `name` | string |  |
| `taskId` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

