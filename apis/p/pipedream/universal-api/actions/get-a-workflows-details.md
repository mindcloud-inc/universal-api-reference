# Pipedream: Get a workflow's details

Retrieves details for a workflow from Pipedream.

```
GET https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-workflows-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-workflows-details?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-workflows-details?${params}`, {
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
| `workflowId` | string | yes | The workflow identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "steps": [
        {}
      ],
      "triggers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `steps` | array<object> |  |
| `triggers` | array<object> |  |

## Native endpoint

Through the native Pipedream API, this operation is `GET /workflows/{workflow_id}` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-workflows-details.md) for the provider-specific parameters and requirements.

