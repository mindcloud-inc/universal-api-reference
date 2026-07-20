# Sapling: Add Dictionary Entry

Adds a custom dictionary entry in Sapling.

```
POST https://connect.mindcloud.co/v1/universal/sapling/latest/actions/add-dictionary-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/add-dictionary-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entry": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sapling/latest/actions/add-dictionary-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entry": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entry` | string | yes | Word or phrase to add to the dictionary. |
| `caseSensitive` | boolean | no | Whether the dictionary entry should be treated as case-sensitive. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case_sensitive": true,
      "created_at": "string",
      "entry": "string",
      "id": "string",
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
| `entry` | string |  |
| `id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/dictionary` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-dictionary-entry.md) for the provider-specific parameters and requirements.

