# OkoCRM: List fields

Retrieves custom fields from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "enums": [
        {}
      ],
      "fields_type_id": 1,
      "id": 1,
      "name": "Ava Chen",
      "system": 1,
      "type": "string",
      "var_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enums` | array<object> |  |
| `fields_type_id` | number |  |
| `id` | number |  |
| `name` | string |  |
| `system` | number |  |
| `type` | string |  |
| `var_name` | string |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /fields/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

