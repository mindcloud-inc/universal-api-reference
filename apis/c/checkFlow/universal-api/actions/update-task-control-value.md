# CheckFlow: Update Task Control Value



```
PUT https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/update-task-control-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/update-task-control-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskContentId": "99",
  "contentId": "55",
  "key": "4cb6f84c-950f-4424-aa7b-d12608419d9b",
  "contentType": "ShortText",
  "name": "Customer Name",
  "value": "Acme Corp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/update-task-control-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskContentId": "99",
    "contentId": "55",
    "key": "4cb6f84c-950f-4424-aa7b-d12608419d9b",
    "contentType": "ShortText",
    "name": "Customer Name",
    "value": "Acme Corp"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskContentId` | number | yes | The ID of the task content record. Example: `99`. |
| `contentId` | number | yes | The ID of the content control. Example: `55`. |
| `key` | string | yes | The key of the content control. Example: `4cb6f84c-950f-4424-aa7b-d12608419d9b`. |
| `contentType` | string | yes | The type of control being updated. Example: `ShortText`. |
| `name` | string | yes | The label or name of the control. Example: `Customer Name`. |
| `value` | string | yes | The value to set. Format depends on the content type. Example: `Acme Corp`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentID": 1,
      "contentType": 1,
      "key": "string",
      "name": "Ava Chen",
      "taskContentID": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentID` | number |  |
| `contentType` | number |  |
| `key` | string |  |
| `name` | string |  |
| `taskContentID` | number |  |
| `value` | string |  |

## Native endpoint

Through the native CheckFlow API, this operation is `PUT /api/task/update-task-content` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-control-value.md) for the provider-specific parameters and requirements.

