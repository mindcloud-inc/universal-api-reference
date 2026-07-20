# Leantime: Get Project Progress



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-project-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-project-progress?connectionId=$CONNECTION_ID&params.projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "params.projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-project-progress?${params}`, {
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
| `params.projectId` | number | yes | The project ID whose progress should be calculated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "estimatedCompletionDate": "string",
      "percent": 1,
      "plannedCompletionDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estimatedCompletionDate` | string |  |
| `percent` | number |  |
| `plannedCompletionDate` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-progress.md) for the provider-specific parameters and requirements.

