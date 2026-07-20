# PostcardMania: Generate Recipient Proof

Creates a proof for a PostcardMania recipient.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/generate-recipient-proof
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/generate-recipient-proof" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/generate-recipient-proof', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientId` | number | yes | Internal recipient identifier. |

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

Through the native PostcardMania API, this operation is `POST /recipient/{{recipientId}}/generate-proof` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-recipient-proof.md) for the provider-specific parameters and requirements.

