# ITM Platform: List Issue Risks



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-issue-risks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-issue-risks?connectionId=$CONNECTION_ID&projectId=string&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "issueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-issue-risks?${params}`, {
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
      "isSelected": true,
      "riskIssueDetail": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSelected` | boolean |  |
| `riskIssueDetail` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/Projects/{ProjectId}/Issues/{IssueId}/Risks` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issue-risks.md) for the provider-specific parameters and requirements.

