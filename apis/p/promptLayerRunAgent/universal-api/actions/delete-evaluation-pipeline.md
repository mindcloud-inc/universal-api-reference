# PromptLayer Run Agent: Delete Evaluation Pipeline

Deletes a PromptLayer evaluation pipeline.

```
DELETE https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/delete-evaluation-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/delete-evaluation-pipeline?connectionId=$CONNECTION_ID&reportId=45407" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "45407"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/delete-evaluation-pipeline?${params}`, {
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
| `reportId` | number | yes | ID of the evaluation pipeline report to archive. Example: `45407`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `DELETE /reports/:reportId` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-evaluation-pipeline.md) for the provider-specific parameters and requirements.

