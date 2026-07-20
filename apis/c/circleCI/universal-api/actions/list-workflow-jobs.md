# CircleCI: List Workflow Jobs



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-workflow-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-workflow-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-workflow-jobs?${params}`, {
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
| `id` | string | no | Opaque workflow identifier. |
| `page-token` | string | no | Pagination cursor returned by CircleCI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "jobNumber": 1,
      "name": "Ava Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `jobNumber` | number |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /workflow/:id/job` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-jobs.md) for the provider-specific parameters and requirements.

