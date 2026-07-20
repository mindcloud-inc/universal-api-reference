# Gridly: Get Column

Retrieves a column from Gridly by column ID.

```
GET https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-column?connectionId=$CONNECTION_ID&viewId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridly/latest/actions/get-column?${params}`, {
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
| `viewId` | string | yes | The unique identifier of the view that contains the column. |
| `id` | string | yes | The unique identifier of the column to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "editable": true,
      "id": "string",
      "isSource": true,
      "isTarget": true,
      "languageCode": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editable` | boolean | Whether the column is editable in the view. |
| `id` | string | Column ID. |
| `isSource` | boolean | Whether the column is a source column. |
| `isTarget` | boolean | Whether the column is a target column. |
| `languageCode` | string | Language code when present. |
| `name` | string | Column name. |
| `type` | string | Column type. |

## Native endpoint

Through the native Gridly API, this operation is `GET /views/:viewId/columns/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-column.md) for the provider-specific parameters and requirements.

