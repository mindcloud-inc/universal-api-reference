# Less Annoying CRM: Get Task



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The task Id to fetch. |

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

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

