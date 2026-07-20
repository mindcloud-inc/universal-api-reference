# xMatters: Get a signal

Retrieves a signal from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-signal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-signal?${params}`, {
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
| `signalId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticatedUser": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "httpResponse": "string",
      "icon": "string",
      "id": "string",
      "payloadType": "string",
      "received": "2026-05-07T12:00:00.000Z",
      "suppressedCount": 1,
      "trigger": {
        "id": "string",
        "name": "Ava Chen",
        "plan": {
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen"
        }
      },
      "triggerLabel": "string",
      "triggerOperation": "string",
      "triggerOutputs": "string",
      "triggerType": "string",
      "workflow": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "name": "Ava Chen"
      },
      "workflowType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticatedUser.firstName` | string |  |
| `authenticatedUser.id` | string |  |
| `authenticatedUser.lastName` | string |  |
| `authenticatedUser.links.self` | string |  |
| `authenticatedUser.recipientType` | string |  |
| `authenticatedUser.targetName` | string |  |
| `httpResponse` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `payloadType` | string |  |
| `received` | date |  |
| `suppressedCount` | number |  |
| `trigger.id` | string |  |
| `trigger.name` | string |  |
| `trigger.plan.id` | string |  |
| `trigger.plan.links.self` | string |  |
| `trigger.plan.name` | string |  |
| `triggerLabel` | string |  |
| `triggerOperation` | string |  |
| `triggerOutputs` | string |  |
| `triggerType` | string |  |
| `workflow.id` | string |  |
| `workflow.links.self` | string |  |
| `workflow.name` | string |  |
| `workflowType` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET signals/{signalId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-signal.md) for the provider-specific parameters and requirements.

