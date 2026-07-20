# Gridly: Update Column

Updates an existing column in a Gridly view.

```
PUT https://connect.mindcloud.co/v1/universal/gridly/latest/actions/update-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/update-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "viewId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridly/latest/actions/update-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "viewId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `viewId` | string | yes | The unique identifier of the view that contains the column. |
| `id` | string | yes | The unique identifier of the column to update. |
| `name` | string | no | The updated name for the column. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no | An updated language code for the column. |
| `localizationType` | string | no | The updated localization role for the column. |
| `numberFormat` | object | no | Updated number-format settings for the column. |
| `selection` | object | no | Updated selection options for the column. |
| `reference` | object | no | Updated reference settings for the column. |
| `formula` | object | no | Updated formula settings for the column. |

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
      "localizationType": "string",
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
| `localizationType` | string | Localization role when present. |
| `name` | string | Column name. |
| `type` | string | Column type. |

## Native endpoint

Through the native Gridly API, this operation is `PATCH /views/:viewId/columns/:id` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-column.md) for the provider-specific parameters and requirements.

