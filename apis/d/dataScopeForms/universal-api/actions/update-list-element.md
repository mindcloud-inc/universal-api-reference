# DataScope Forms: Update List Element

Updates an existing list element in DataScope Forms.

```
PUT https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/update-list-element
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/update-list-element" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/update-list-element', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Internal identifier of the list element to update. |
| `list_object.attribute1` | string | no | First custom attribute of the list element. |
| `list_object.attribute2` | string | no | Second custom attribute of the list element. |
| `list_object.code` | string | no | Internal code of the list element. |
| `list_object.description` | string | no | Description of the list element. |
| `list_object.name` | string | no | Name of the list element. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attribute1": "string",
      "attribute2": "string",
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "metadata_type": "string",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attribute1` | string |  |
| `attribute2` | string |  |
| `code` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `metadata_type` | string |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native DataScope Forms API, this operation is `POST /external/metadata_object/[:id]` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list-element.md) for the provider-specific parameters and requirements.

