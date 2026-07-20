# Gridly: Create Column

Creates a new column in a Gridly view.

```
POST https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "viewId": "string",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gridly/latest/actions/create-column', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "viewId": "string",
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `viewId` | string | yes | The unique identifier of the view where the column should be created. |
| `name` | string | yes | The display name of the column to create. |
| `type` | string | yes | The Gridly column type to create. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | An optional explicit column ID to assign when creating the column. |
| `languageCode` | string | no | A language code for language columns. |
| `localizationType` | string | no | The localization role for language columns, such as sourceLanguage or targetLanguage. |
| `numberFormat` | object | no | Number-format settings for number columns. |
| `selection` | object | no | Selection options for singleSelection or multipleSelections columns. |
| `reference` | object | no | Reference settings for reference columns. |
| `formula` | object | no | Formula settings for formula columns. |

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

Through the native Gridly API, this operation is `POST /views/:viewId/columns` (base URL `https://api.gridly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-column.md) for the provider-specific parameters and requirements.

