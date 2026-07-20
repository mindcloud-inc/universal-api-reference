# Clicksign: Create Qualification Requirement

Creates a qualification requirement in Clicksign.

```
POST https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-qualification-requirement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-qualification-requirement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.role": "string",
  "data.relationships.document.data.id": "string",
  "data.relationships.signer.data.id": "string",
  "envelopeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/create-qualification-requirement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.role": "string",
    "data.relationships.document.data.id": "string",
    "data.relationships.signer.data.id": "string",
    "envelopeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | JSON:API document wrapper. |
| `data.attributes` | object | no | Requirement attributes. |
| `data.attributes.role` | string | yes | The signer role used by the requirement. |
| `data.relationships` | object | no | Requirement relationships. |
| `data.relationships.document` | object | no | Target document relationship. |
| `data.relationships.document.data` | object | no | JSON:API document relationship wrapper. |
| `data.relationships.document.data.id` | string | yes | The UUID of the related document. |
| `data.relationships.signer` | object | no | Target signer relationship. |
| `data.relationships.signer.data` | object | no | JSON:API signer relationship wrapper. |
| `data.relationships.signer.data.id` | string | yes | The UUID of the related signer. |
| `envelopeId` | string | yes | The UUID of the envelope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `POST /envelopes/:envelope_id/requirements` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qualification-requirement.md) for the provider-specific parameters and requirements.

