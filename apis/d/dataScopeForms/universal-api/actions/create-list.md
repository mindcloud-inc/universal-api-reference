# DataScope Forms: Create List

Creates a new list in DataScope Forms.

```
POST https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/create-list', {
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
| `list.code` | string | no | Internal code of the list. |
| `list.description` | string | no | Description of the list. |
| `list.list_type` | string | no | Type of the list. Valid values: standard, percent, price. |
| `list.name` | string | no | Name of the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "description": "string",
      "id": 1,
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
| `list_type` | string |  |
| `name` | string |  |

## Native endpoint

Through the native DataScope Forms API, this operation is `POST /external/metadata_types` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

