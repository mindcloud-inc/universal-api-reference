# Chatvolt AI: List Dispatches

Retrieves dispatches from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/dispatches-get?${params}`, {
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
| `offset` | number | no | Number of records to skip for pagination. |
| `limit` | number | no | Maximum number of records to return. |
| `search` | string | no | Search term for dispatch name. |
| `status` | string | no | Filter by dispatch status. |
| `agentId` | string | no | Filter by Agent ID. |
| `crmScenarioId` | string | no | Filter by CRM Scenario ID. |
| `crmStepId` | string | no | Filter by CRM Step ID. |
| `startDate` | string | no | Filter dispatches scheduled on or after this date. |
| `endDate` | string | no | Filter dispatches scheduled on or before this date. |
| `archived` | boolean | no | Filter by archived status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "dispatches": [
        "string"
      ],
      "errorCount": 1,
      "latestErrorMessage": "string",
      "sentCount": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Count. |
| `dispatches` | array | Dispatches. |
| `errorCount` | number | ErrorCount. |
| `latestErrorMessage` | string | LatestErrorMessage. |
| `sentCount` | number | SentCount. |
| `totalCount` | number | TotalCount. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /dispatches` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dispatches-get.md) for the provider-specific parameters and requirements.

