# Formitize: Get Task

Retrieves a task from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-task?${params}`, {
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
| `id` | string | no | Formitize task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": 1,
      "attachments": [
        {}
      ],
      "createdBy": 1,
      "dateCreated": 1,
      "dateModified": 1,
      "description": "string",
      "dueDate": 1,
      "id": 1,
      "relatedTo": {},
      "status": 1,
      "tags": [
        "string"
      ],
      "taskType": "string",
      "title": "string",
      "workflow": [
        {}
      ],
      "workflowID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | number |  |
| `attachments` | array<object> |  |
| `createdBy` | number |  |
| `dateCreated` | number |  |
| `dateModified` | number |  |
| `description` | string |  |
| `dueDate` | number |  |
| `id` | number |  |
| `relatedTo` | object |  |
| `status` | number |  |
| `tags` | array<string> |  |
| `taskType` | string |  |
| `title` | string |  |
| `workflow` | array<object> |  |
| `workflowID` | number |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /crm/task/:id` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

