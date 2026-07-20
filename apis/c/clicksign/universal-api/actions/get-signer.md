# Clicksign: Get Signer

Retrieves a signer from Clicksign.

```
GET https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/get-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/get-signer?connectionId=$CONNECTION_ID&envelopeId=string&signerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string",
  "signerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/get-signer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `envelopeId` | string | yes | The UUID of the envelope. |
| `signerId` | string | yes | The UUID of the signer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `GET /envelopes/:envelope_id/signers/:signer_id` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signer.md) for the provider-specific parameters and requirements.

