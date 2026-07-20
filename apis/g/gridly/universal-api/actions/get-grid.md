# Gridly: Get Grid

Retrieves a grid from Gridly by grid ID.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-grid?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-grid?${params}`, {
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
| `id` | string | yes | The unique identifier of the grid to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {}
      ],
      "defaultAccessViewId": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "recordIdentifierType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> | Columns configured in the grid. |
| `defaultAccessViewId` | string | Default view ID for the grid. |
| `id` | string | Grid ID. |
| `metadata` | object | Grid metadata. |
| `name` | string | Grid name. |
| `recordIdentifierType` | string | Record identifier strategy. |
| `status` | string | Grid status. |

## Native endpoint

Through the native Gridly API, this operation is `GET /grids/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-grid.md) for the provider-specific parameters and requirements.

