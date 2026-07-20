# Sapling: Add Custom Mapping

Adds a custom mapping in Sapling.

```
POST https://connect.mindcloud.co/v1/universal/sapling/latest/actions/add-custom-mapping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/add-custom-mapping" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entry": "string",
  "mapping": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sapling/latest/actions/add-custom-mapping', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entry": "string",
    "mapping": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entry` | string | yes | Word or pattern to match. |
| `mapping` | string | yes | Replacement text to suggest. |
| `caseSensitive` | boolean | no | Whether the mapping match is case-sensitive. Default: `false`. |
| `description` | string | no | Optional explanation shown with the mapping. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case_sensitive": true,
      "created_at": "string",
      "description": "string",
      "entry": "string",
      "id": "string",
      "mapping": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case_sensitive` | boolean |  |
| `created_at` | string |  |
| `description` | string |  |
| `entry` | string |  |
| `id` | string |  |
| `mapping` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/custom_mapping` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-mapping.md) for the provider-specific parameters and requirements.

