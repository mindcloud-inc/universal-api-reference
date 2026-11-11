# MindCloud: List Run Operations



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-run-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-run-operations?connectionId=$CONNECTION_ID&limit=25&offset=0&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-run-operations?${params}`, {
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
| `runId` | string | yes | Run ID for this MindCloud v2 request. |
| `where` | string | no | Optional Where query parameter documented by the MindCloud v2 API. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated fields to return. Leave empty to return all fields. The API always includes id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned records. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native MindCloud API, this operation is `GET /v2/runs/:runId/operations` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-run-operations.md) for the provider-specific parameters and requirements.

