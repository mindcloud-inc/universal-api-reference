# MoreApp: Create Task

Creates a task in MoreApp.

```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "209321",
  "data": {
    "fullName": "MindCloud App"
  },
  "formId": "69bc27abd8b8b4ce5be6b2ba",
  "message": "Please fill in this MindCloud test task.",
  "publishInfo": {
    "type": "IMMEDIATE",
    "value": 0
  },
  "recipients[]": [
    "apps@mindcloud.co"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "209321",
    "data": {"fullName":"MindCloud App"},
    "formId": "69bc27abd8b8b4ce5be6b2ba",
    "message": "Please fill in this MindCloud test task.",
    "publishInfo": {"type":"IMMEDIATE","value":0},
    "recipients[]": ["apps@mindcloud.co"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `data` | object | yes | Form data payload for the task. Default: `{"fullName":"MindCloud App"}`. |
| `formId` | string | yes | MoreApp form identifier. Default: `69bc27abd8b8b4ce5be6b2ba`. |
| `message` | string | yes | Task message. Default: `Please fill in this MindCloud test task.`. |
| `publishInfo` | object | yes | Task publish scheduling object. Default: `{"type":"IMMEDIATE","value":0}`. |
| `recipients[]` | array<string> | yes | Email recipients for the task. Accepts multiple values as an array. Default: `["apps@mindcloud.co"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "customerId": 1,
      "data": {},
      "dates": {},
      "description": "string",
      "formId": "string",
      "formName": "Ava Chen",
      "fulfilments": [
        {}
      ],
      "id": "string",
      "location": {},
      "message": "string",
      "status": "string",
      "taskUsers": [
        {}
      ],
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | object |  |
| `customerId` | number |  |
| `data` | object |  |
| `dates` | object |  |
| `description` | string |  |
| `formId` | string |  |
| `formName` | string |  |
| `fulfilments` | array<object> |  |
| `id` | string |  |
| `location` | object |  |
| `message` | string |  |
| `status` | string |  |
| `taskUsers` | array<object> |  |
| `users` | array<string> |  |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

