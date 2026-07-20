# Gridly: Create View

Creates a new view in Gridly.

```
POST https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "gridId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "gridId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the view to create. |
| `gridId` | string | yes | The unique identifier of the grid that the new view belongs to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns[]` | array<object> | no | An optional list of existing columns to add to the view when creating it. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {}
      ],
      "gridId": "string",
      "gridStatus": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> | Columns included in the view. |
| `gridId` | string | Owning grid ID. |
| `gridStatus` | string | Owning grid status. |
| `id` | string | View ID. |
| `name` | string | View name. |

## Native endpoint

Through the native Gridly API, this operation is `POST /views` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-view.md) for the provider-specific parameters and requirements.

