# Zite: Create Field

Creates a new field in a Zite table.

```
POST https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-field', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "template": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `order` | number |  |
| `template` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Zite API, this operation is `POST /bases/:databaseId/tables/:tableId/fields` (base URL `https://tables.fillout.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

