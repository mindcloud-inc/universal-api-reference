# GoCanvas: Retrieve Workflow



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-workflow?connectionId=$CONNECTION_ID&workflowId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-workflow?${params}`, {
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
| `workflowId` | number | yes | Identifier of the workflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedNotificationReceiver": "string",
      "completedNotificationType": "string",
      "formId": 1,
      "id": 1,
      "initalStateName": "Ava Chen",
      "submissionOwnerFlag": "string",
      "type": "string",
      "versionNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedNotificationReceiver` | string |  |
| `completedNotificationType` | string |  |
| `formId` | number |  |
| `id` | number |  |
| `initalStateName` | string |  |
| `submissionOwnerFlag` | string |  |
| `type` | string |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /workflows/:workflowId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-workflow.md) for the provider-specific parameters and requirements.

