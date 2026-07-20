# Merit: Create Item



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes | Array of item objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "ItemId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | Created item code. |
| `ItemId` | string | Created item identifier. |

## Native endpoint

Through the native Merit API, this operation is `POST v2/senditems` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

