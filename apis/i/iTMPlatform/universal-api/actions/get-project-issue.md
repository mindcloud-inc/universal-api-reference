# ITM Platform: Get Project Issue



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-issue?connectionId=$CONNECTION_ID&projectId=string&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "issueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-issue?${params}`, {
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
      "accountId": 1,
      "description": "string",
      "id": 1,
      "isConsiderActionTaskCost": true,
      "languageId": 1,
      "name": "Ava Chen",
      "no": "string",
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `isConsiderActionTaskCost` | boolean |  |
| `languageId` | number |  |
| `name` | string |  |
| `no` | string |  |
| `projectId` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/Projects/{ProjectId}/Issues/{IssueId}` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-issue.md) for the provider-specific parameters and requirements.

