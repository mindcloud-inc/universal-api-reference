# SavvyCal: List Workflow Rules



```
GET https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-workflow-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-workflow-rules?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-workflow-rules?${params}`, {
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
| `workflowId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "properties": {
            "recipient": "string",
            "template": "string"
          },
          "type": "string"
        }
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "triggerOffsetAmount": 1,
      "triggerOffsetDirection": "string",
      "triggerOffsetUnit": "string",
      "triggerType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions[].createdAt` | date | When the workflow action was created. |
| `actions[].id` | string | Workflow action identifier. |
| `actions[].properties.recipient` | string | Workflow action recipient. |
| `actions[].properties.template` | string | Workflow action template. |
| `actions[].type` | string | Workflow action type. |
| `createdAt` | date | When the workflow rule was created. |
| `id` | string | Unique workflow rule identifier. |
| `triggerOffsetAmount` | number | Trigger offset amount. |
| `triggerOffsetDirection` | string | Trigger offset direction. |
| `triggerOffsetUnit` | string | Trigger offset unit. |
| `triggerType` | string | Rule trigger type. |

## Native endpoint

Through the native SavvyCal API, this operation is `GET /v1/workflows/:workflow_id/rules` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-rules.md) for the provider-specific parameters and requirements.

