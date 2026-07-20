# Elastic Cloud: Get Deployment Certificate Authority

Retrieves a deployment certificate authority from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-certificate-authority
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-certificate-authority?connectionId=$CONNECTION_ID&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-certificate-authority?${params}`, {
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
| `deploymentId` | string | yes | Identifier for the deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "publicCertificates": [
        {
          "active": true,
          "metadata": {
            "fingerprint": "string",
            "validFrom": "2026-05-07T12:00:00.000Z",
            "validTo": "2026-05-07T12:00:00.000Z"
          },
          "pem": "string"
        }
      ],
      "recommendedTrustRestriction": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publicCertificates[].active` | boolean |  |
| `publicCertificates[].metadata.fingerprint` | string |  |
| `publicCertificates[].metadata.validFrom` | date |  |
| `publicCertificates[].metadata.validTo` | date |  |
| `publicCertificates[].pem` | string |  |
| `recommendedTrustRestriction` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/:deployment_id/certificate-authority` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-certificate-authority.md) for the provider-specific parameters and requirements.

