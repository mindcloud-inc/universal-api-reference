# xMatters: Get signals

Retrieves signals from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-signals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-signals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-signals?${params}`, {
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
| `groupId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
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
            "integrationConfigType": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen"
          },
          "workflowType": "string"
        }
      ],
      "links": {
        "next": "https://example.com",
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].authenticatedUser.firstName` | string |  |
| `data[].authenticatedUser.id` | string |  |
| `data[].authenticatedUser.lastName` | string |  |
| `data[].authenticatedUser.links.self` | string |  |
| `data[].authenticatedUser.recipientType` | string |  |
| `data[].authenticatedUser.targetName` | string |  |
| `data[].httpResponse` | string |  |
| `data[].icon` | string |  |
| `data[].id` | string |  |
| `data[].payloadType` | string |  |
| `data[].received` | date |  |
| `data[].suppressedCount` | number |  |
| `data[].trigger.id` | string |  |
| `data[].trigger.name` | string |  |
| `data[].trigger.plan.id` | string |  |
| `data[].trigger.plan.links.self` | string |  |
| `data[].trigger.plan.name` | string |  |
| `data[].triggerLabel` | string |  |
| `data[].triggerOperation` | string |  |
| `data[].triggerOutputs` | string |  |
| `data[].triggerType` | string |  |
| `data[].workflow.id` | string |  |
| `data[].workflow.integrationConfigType` | string |  |
| `data[].workflow.links.self` | string |  |
| `data[].workflow.name` | string |  |
| `data[].workflowType` | string |  |
| `links.next` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}/signals` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-signals.md) for the provider-specific parameters and requirements.

