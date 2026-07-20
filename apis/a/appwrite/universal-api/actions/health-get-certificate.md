# Appwrite: Get the SSL certificate for a domain

Retrieves Appwrite SSL certificate details for a domain.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-certificate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/health-get-certificate?${params}`, {
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
| `domain` | string | no | string |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issuerOrganisation": "string",
      "name": "Ava Chen",
      "signatureTypeSN": "string",
      "subjectSN": "string",
      "validFrom": "string",
      "validTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issuerOrganisation` | string | Issuer organisation |
| `name` | string | Certificate name |
| `signatureTypeSN` | string | Signature type SN |
| `subjectSN` | string | Subject SN |
| `validFrom` | string | Valid from |
| `validTo` | string | Valid to |

## Native endpoint

Through the native Appwrite API, this operation is `GET /health/certificate` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-get-certificate.md) for the provider-specific parameters and requirements.

