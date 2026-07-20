# Gridly: List Dependencies

Finds dependencies in a specific Gridly view.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-dependencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-dependencies?connectionId=$CONNECTION_ID&viewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-dependencies?${params}`, {
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
| `viewId` | string | yes | The unique identifier of the view whose dependencies you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "sourceColumnId": "string",
      "targetColumnId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Dependency ID. |
| `sourceColumnId` | string | Source column ID. |
| `targetColumnId` | string | Target column ID. |

## Native endpoint

Through the native Gridly API, this operation is `GET /views/:viewId/dependencies` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dependencies.md) for the provider-specific parameters and requirements.

