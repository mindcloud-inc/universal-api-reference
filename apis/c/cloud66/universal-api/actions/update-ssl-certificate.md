# Cloud 66: Update SSL Certificate

Updates an SSL certificate in your Cloud 66 account.

```
PUT https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/update-ssl-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/update-ssl-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string",
  "id": "string",
  "sslCertificate.serverNames": "Ava Chen",
  "sslCertificate.sslTermination": true,
  "sslCertificate.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/update-ssl-certificate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string",
    "id": "string",
    "sslCertificate.serverNames": "Ava Chen",
    "sslCertificate.sslTermination": true,
    "sslCertificate.type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes | Unique identifier of the stack |
| `id` | string | yes | SSL certificate ID |
| `sslCertificate` | object | no | SSL certificate payload |
| `sslCertificate.serverNames` | string | yes | Comma separated list of domains |
| `sslCertificate.sslTermination` | boolean | yes | Whether the certificate is terminated on the load balancer |
| `sslCertificate.type` | string | yes | Type of certificate: manual or lets_encrypt |
| `sslCertificate.certificate` | string | no | Required for manual certificates |
| `sslCertificate.key` | string | no | Required for manual certificates |
| `sslCertificate.intermediateCertificate` | string | no | Intermediate certificate chain |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sslCertificate.wildcard` | boolean | no | Only applies to lets_encrypt wildcard certificates |
| `sslCertificate.dnsProviderUuid` | string | no | Required for wildcard lets_encrypt certificates |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `PATCH /stacks/:stack_id/ssl_certificates/:id` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ssl-certificate.md) for the provider-specific parameters and requirements.

