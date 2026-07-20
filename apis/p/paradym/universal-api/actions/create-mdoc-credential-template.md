# Paradym: Create Mdoc Credential Template

Creates an mdoc credential template in Paradym.

```
POST https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-mdoc-credential-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-mdoc-credential-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Test Mdoc 20260402",
  "type": "org.mindcloud.test.card",
  "validUntil.future.years": "1",
  "issuer.keyType": "0",
  "attributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-mdoc-credential-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Test Mdoc 20260402",
    "type": "org.mindcloud.test.card",
    "validUntil.future.years": "1",
    "issuer.keyType": "0",
    "attributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Template name. Example: `MindCloud Test Mdoc 20260402`. |
| `description` | string | no | Optional template description. Example: `Runtime test template`. |
| `type` | string | yes | Credential type identifier for the mdoc template. Example: `org.mindcloud.test.card`. |
| `validUntil.future.years` | number | yes | Number of years after issuance that the credential remains valid. Example: `1`. |
| `issuer.keyType` | string | yes | Certificate key type used for issuance. One of: `0`, `1`. |
| `attributes` | object | yes | Attributes schema object keyed by credential namespace. Example: {"org.mindcloud.test.card":{"properties":{"fullName":{"type":"string","name":"Full Name","required":true}}}} |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `POST /projects/:projectId/templates/credentials/mdoc` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mdoc-credential-template.md) for the provider-specific parameters and requirements.

