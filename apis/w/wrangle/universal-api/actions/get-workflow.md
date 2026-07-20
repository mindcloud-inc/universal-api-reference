# Wrangle: Get Workflow



```
GET https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-workflow?connectionId=$CONNECTION_ID&workflowId=workflow_uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "workflow_uuid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-workflow?${params}`, {
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
| `workflowId` | string | yes | The Wrangle workflow ID. Example: `workflow_uuid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "workflow": {
        "id": "string",
        "intakeFormFields": [
          {
            "fieldId": "string",
            "fieldLabel": "string",
            "fieldType": "string",
            "isRequired": true
          }
        ],
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `workflow.id` | string |  |
| `workflow.intakeFormFields[].fieldId` | string |  |
| `workflow.intakeFormFields[].fieldLabel` | string |  |
| `workflow.intakeFormFields[].fieldType` | string |  |
| `workflow.intakeFormFields[].isRequired` | boolean |  |
| `workflow.name` | string |  |

## Native endpoint

Through the native Wrangle API, this operation is `GET /workflows/:workflowId` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

