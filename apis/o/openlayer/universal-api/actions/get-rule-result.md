# Openlayer: Get Rule Result

Retrieves a rule result from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-rule-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-rule-result?connectionId=$CONNECTION_ID&ruleResultId=ddc5207c-9b56-47a1-a273-1c5068867b6d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ruleResultId": "ddc5207c-9b56-47a1-a273-1c5068867b6d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-rule-result?${params}`, {
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
| `ruleResultId` | string | yes | Openlayer rule result ID. Default: `ddc5207c-9b56-47a1-a273-1c5068867b6d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
      "dateLastEvaluated": "string",
      "dateOfNextEvaluation": "string",
      "dateUpdated": "string",
      "id": "string",
      "projectId": "string",
      "ruleId": "string",
      "status": "string",
      "statusMessage": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `dateLastEvaluated` | string |  |
| `dateOfNextEvaluation` | string |  |
| `dateUpdated` | string |  |
| `id` | string |  |
| `projectId` | string |  |
| `ruleId` | string |  |
| `status` | string |  |
| `statusMessage` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /rule-results/:ruleResultId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rule-result.md) for the provider-specific parameters and requirements.

