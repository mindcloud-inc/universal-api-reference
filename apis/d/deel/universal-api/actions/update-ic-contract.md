# Deel: Update IC Contract

Updates an existing IC contract in Deel.

```
PUT https://connect.mindcloud.co/v1/universal/deel/latest/actions/update-ic-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/deel/latest/actions/update-ic-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deel/latest/actions/update-ic-contract', {
  method: 'PUT',
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Deel API, this operation is `PATCH /contracts/:contract_id` (base URL `https://api.letsdeel.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ic-contract.md) for the provider-specific parameters and requirements.

