# ITM Platform: Get Risk Occurrence Management



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-risk-occurrence-management
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-risk-occurrence-management?connectionId=$CONNECTION_ID&projectId=string&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "issueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-risk-occurrence-management?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |
| `issueId` | string | yes | The ITM Platform issue ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalRiskOccurenceCost": 1,
      "totalScheduleVariance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalRiskOccurenceCost` | number |  |
| `totalScheduleVariance` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/Issue/{IssueId}/riskoccurencemanagement` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-risk-occurrence-management.md) for the provider-specific parameters and requirements.

