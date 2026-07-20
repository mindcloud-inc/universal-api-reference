# Gridly: Create Grid

Creates a new grid in Gridly.

```
POST https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-grid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dbId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-grid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dbId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dbId` | string | yes | The unique identifier of the database where the grid should be created. |
| `name` | string | no | The name of the grid to create. |
| `templateGridId` | string | no | An existing Gridly template grid ID to create from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | A metadata object to store with the grid. |

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
| `defaultAccessViewId` | string | Default access view ID. |
| `id` | string | Grid ID. |
| `metadata` | object | Grid metadata. |
| `name` | string | Grid name. |
| `recordIdentifierType` | string | Record identifier strategy. |
| `status` | string | Grid status. |

## Native endpoint

Through the native Gridly API, this operation is `POST /grids` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-grid.md) for the provider-specific parameters and requirements.

