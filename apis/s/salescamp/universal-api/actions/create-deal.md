# Salescamp: Create Deal



```
POST https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salescamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Deal name |
| `value` | number | no | Deal value |
| `status` | string | no | Deal status |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
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

## Native endpoint

Through the native Salescamp API, this operation is `POST /v1/collections/69cd24c3f24a3ccfd974bb19/items` (base URL `https://api.salescamp.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

