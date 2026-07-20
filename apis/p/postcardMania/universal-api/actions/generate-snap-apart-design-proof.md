# PostcardMania: Generate Snap Apart Design Proof

Creates a snap-apart design proof in PostcardMania.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/generate-snap-apart-design-proof
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/generate-snap-apart-design-proof" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/generate-snap-apart-design-proof', {
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
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf` | string | Temporary PDF URL for the generated proof. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /design/generate-proof/snap-apart` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-snap-apart-design-proof.md) for the provider-specific parameters and requirements.

