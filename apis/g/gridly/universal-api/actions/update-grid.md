# Gridly: Update Grid

Updates an existing grid in Gridly.

```
PUT https://connect.mindcloud.co/v1/universal/gridly/latest/actions/update-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/update-grid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridly/latest/actions/update-grid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the grid to update. |
| `name` | string | no | The new name for the grid. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | A metadata object to update on the grid. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `defaultAccessViewId` | string | Default access view ID. |
| `id` | string | Grid ID. |
| `metadata` | object | Grid metadata. |
| `name` | string | Grid name. |
| `recordIdentifierType` | string | Record identifier strategy. |
| `status` | string | Grid status. |

## Native endpoint

Through the native Gridly API, this operation is `PATCH /grids/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-grid.md) for the provider-specific parameters and requirements.

