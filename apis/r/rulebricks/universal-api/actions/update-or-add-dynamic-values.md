# Rulebricks: Update or Add Dynamic Values

Updates or adds dynamic values in Rulebricks.

```
PUT https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/update-or-add-dynamic-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/update-or-add-dynamic-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/update-or-add-dynamic-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "values": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user_groups[]` | array<string> | no | Optional array of user group names or IDs |
| `values` | object | yes | Dictionary of keys and values to update or add |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
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
| `id` | string | Value ID |
| `name` | string | Value name |
| `type` | string | Stored value type |

## Native endpoint

Through the native Rulebricks API, this operation is `POST /values` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-or-add-dynamic-values.md) for the provider-specific parameters and requirements.

