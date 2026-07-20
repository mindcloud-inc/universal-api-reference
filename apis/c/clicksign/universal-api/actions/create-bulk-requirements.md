# Clicksign: Create Bulk Requirements

Creates bulk requirements in a Clicksign envelope.

```
POST https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-bulk-requirements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-bulk-requirements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "atomic:operations[]": [
    {}
  ],
  "envelopeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-bulk-requirements', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "atomic:operations[]": [{}],
    "envelopeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `atomic:operations[]` | array<object> | yes | The JSON:API atomic operations array used for bulk requirement creation. |
| `envelopeId` | string | yes | The UUID of the envelope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `POST /envelopes/:envelope_id/bulk_requirements` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-requirements.md) for the provider-specific parameters and requirements.

