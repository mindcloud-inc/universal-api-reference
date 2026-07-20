# Deel: Create Contract Document

Attaches a document to a contract in Deel.

```
POST https://connect.mindcloud.co/v1/universal/deel/latest/actions/create-contract-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deel/latest/actions/create-contract-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deel/latest/actions/create-contract-document', {
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

Through the native Deel API, this operation is `POST /contracts/:contract_id/documents` (base URL `https://api.letsdeel.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract-document.md) for the provider-specific parameters and requirements.

