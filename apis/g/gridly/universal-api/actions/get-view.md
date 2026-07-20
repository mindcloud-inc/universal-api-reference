# Gridly: Get View

Retrieves a view from Gridly by view ID.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-view?${params}`, {
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
| `id` | string | yes | ID of the view. It can be found in the API quick start right panel of your Gridly Dashboard. |

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
| `columns` | array<object> | Columns visible in the view. |
| `gridId` | string | Owning grid ID. |
| `gridStatus` | string | Owning grid status. |
| `id` | string | View ID. |
| `name` | string | View name. |

## Native endpoint

Through the native Gridly API, this operation is `GET /views/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-view.md) for the provider-specific parameters and requirements.

