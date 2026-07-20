# DataScope Forms: Create List Element

Creates a new list element in DataScope Forms.

```
POST https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-list-element
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-list-element" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-list-element', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_object.attribute1` | string | no | First custom attribute of the list element. |
| `list_object.attribute2` | string | no | Second custom attribute of the list element. |
| `list_object.code` | string | no | Internal code of the list element. |
| `list_object.description` | string | no | Description of the list element. |
| `list_object.name` | string | no | Name of the list element. |
| `metadata_type` | string | no | Internal code that identifies the target list. |

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

Through the native DataScope Forms API, this operation is `POST /external/metadata_object` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-element.md) for the provider-specific parameters and requirements.

