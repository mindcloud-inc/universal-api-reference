# Intradesk: List Workflow Transition Statuses

Retrieves workflow transition statuses from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-workflow-transition-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-workflow-transition-statuses?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-workflow-transition-statuses?${params}`, {
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
| `workflowId` | string | yes | Workflow identifier from Intradesk Rules API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buttonName": "Ava Chen",
      "fromId": 1,
      "toId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buttonName` | string |  |
| `fromId` | number |  |
| `toId` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /changes/api/Rules/transitionstatuses/{workflowId}` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-transition-statuses.md) for the provider-specific parameters and requirements.

