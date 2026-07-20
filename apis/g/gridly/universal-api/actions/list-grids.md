# Gridly: List Grids

Finds grids in Gridly by database ID.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-grids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-grids?connectionId=$CONNECTION_ID&dbId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dbId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/list-grids?${params}`, {
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
| `dbId` | string | yes | The unique identifier of the database whose grids you want to list. |

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
| `defaultAccessViewId` | string | Default view ID for the grid. |
| `id` | string | Grid ID. |
| `metadata` | object | Grid metadata. |
| `name` | string | Grid name. |
| `recordIdentifierType` | string | Record identifier strategy. |
| `status` | string | Grid status. |

## Native endpoint

Through the native Gridly API, this operation is `GET /grids` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-grids.md) for the provider-specific parameters and requirements.

