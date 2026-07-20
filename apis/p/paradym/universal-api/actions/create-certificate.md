# Paradym: Create Certificate

Creates a certificate in Paradym.

```
POST https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issuerAlternativeNameUrl": "https://mindcloud.co",
  "countryName": "BR",
  "keyType": "0",
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paradym/latest/actions/create-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issuerAlternativeNameUrl": "https://mindcloud.co",
    "countryName": "BR",
    "keyType": "0",
    "type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issuerAlternativeNameUrl` | string | yes | Issuer alternative name URL for the certificate. Example: `https://mindcloud.co`. |
| `countryName` | string | yes | Two-letter country code for the certificate subject. Example: `BR`. |
| `keyType` | string | yes | Cryptographic key type for the certificate. One of: `0`, `1`. |
| `type` | string | yes | Paradym certificate purpose. One of: `0`, `1`. |
| `commonName` | string | no | Optional common name for the certificate subject. Example: `MindCloud Test Certificate`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paradym API returns.

## Native endpoint

Through the native Paradym API, this operation is `POST /projects/:projectId/certificates` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-certificate.md) for the provider-specific parameters and requirements.

