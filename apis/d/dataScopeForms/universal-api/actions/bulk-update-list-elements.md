# DataScope Forms: Bulk Update List Elements

Updates list elements in DataScope Forms by replacing the full list.

```
PUT https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/bulk-update-list-elements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/bulk-update-list-elements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_objects[]": [
    {}
  ],
  "metadata_type": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/bulk-update-list-elements', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_objects[]": [{}],
    "metadata_type": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_objects[]` | array<object> | yes | Array of list objects to create or update. Objects not present may be soft-deleted by DataScope. |
| `metadata_type` | string | yes | Internal code that identifies the list to replace. |
| `name` | string | yes | Name of the list to create or update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "description": "string",
      "id": 1,
      "length": 1,
      "list_type": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `description` | string |  |
| `id` | number |  |
| `length` | number |  |
| `list_type` | string |  |
| `name` | string |  |

## Native endpoint

Through the native DataScope Forms API, this operation is `POST /external/metadata_objects/bulk_update` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-list-elements.md) for the provider-specific parameters and requirements.

