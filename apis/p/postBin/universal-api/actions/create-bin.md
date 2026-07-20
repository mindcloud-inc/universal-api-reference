# PostBin: Create Bin

Creates a new PostBin bin.

```
POST https://connect.mindcloud.co/v1/universal/postBin/latest/actions/create-bin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostBin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/create-bin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postBin/latest/actions/create-bin', {
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
      "binId": "string",
      "expires": 1,
      "now": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binId` | string | Opaque identifier for the temporary bin. |
| `expires` | number | UTC timestamp in milliseconds when the bin expires. |
| `now` | number | UTC timestamp in milliseconds when the bin was created. |

## Native endpoint

Through the native PostBin API, this operation is `POST /bin` (base URL `https://www.postb.in/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bin.md) for the provider-specific parameters and requirements.

