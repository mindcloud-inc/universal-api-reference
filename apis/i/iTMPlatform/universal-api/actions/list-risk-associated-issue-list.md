# ITM Platform: List Risk Associated Issue List



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-risk-associated-issue-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-risk-associated-issue-list?connectionId=$CONNECTION_ID&projectId=string&riskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "riskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-risk-associated-issue-list?${params}`, {
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
| `riskId` | string | yes | The ITM Platform risk ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affectedIssues": [
        {}
      ],
      "riskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affectedIssues` | array<object> |  |
| `riskId` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/Risk/{RiskId}/AssociatedIssueList` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-risk-associated-issue-list.md) for the provider-specific parameters and requirements.

