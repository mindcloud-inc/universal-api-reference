# Shuffler: List Workflow Executions

Retrieves workflow executions from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-workflow-executions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-workflow-executions?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-workflow-executions?${params}`, {
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
| `workflowId` | string | yes | Workflow Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "executions": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `executions` | array |  |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `GET /workflows/{workflowId}/executions` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-executions.md) for the provider-specific parameters and requirements.

