# Zahara: List Workflows

Retrieves workflows from a Zahara business unit.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-workflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessDivisionId": 1,
      "ConditionalStart": true,
      "Id": 1,
      "IsAdHocWorkflow": true,
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "ProcessId": 1,
      "ProcessSteps": [
        {
          "ConditionalStart": true,
          "FullyQualifiedName": "Ava Chen",
          "Index": 1,
          "LastUpdated": "2026-05-07T12:00:00.000Z",
          "Name": "Ava Chen",
          "ProcessId": 1,
          "ProcessStepId": 1,
          "RevisionNumber": 1,
          "StartConditions": "string",
          "StepObjectData": "string"
        }
      ],
      "ProcessType": 1,
      "RevisionNumber": 1,
      "StartConditions": "string",
      "Void": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessDivisionId` | number | Business division ID. |
| `ConditionalStart` | boolean | Whether the workflow has conditional start logic. |
| `Id` | number | Workflow ID. |
| `IsAdHocWorkflow` | boolean | Whether the workflow is ad hoc. |
| `LastUpdated` | date | Last update timestamp. |
| `Name` | string | Workflow name. |
| `ProcessId` | number | Workflow process ID. |
| `ProcessSteps[].ConditionalStart` | boolean | Whether the workflow step is conditional. |
| `ProcessSteps[].FullyQualifiedName` | string | Workflow step implementation type. |
| `ProcessSteps[].Index` | number | Workflow step order index. |
| `ProcessSteps[].LastUpdated` | date | Workflow step last update timestamp. |
| `ProcessSteps[].Name` | string | Workflow step name. |
| `ProcessSteps[].ProcessId` | number | Workflow step process ID. |
| `ProcessSteps[].ProcessStepId` | number | Workflow step ID. |
| `ProcessSteps[].RevisionNumber` | number | Workflow step revision number. |
| `ProcessSteps[].StartConditions` | string | Workflow step start conditions XML. |
| `ProcessSteps[].StepObjectData` | string | Workflow step configuration payload. |
| `ProcessType` | number | Workflow process type. |
| `RevisionNumber` | number | Workflow revision number. |
| `StartConditions` | string | Workflow start conditions XML. |
| `Void` | boolean | Whether the workflow is void. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.businessUnitApiKey}}/Process/GetAll` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

