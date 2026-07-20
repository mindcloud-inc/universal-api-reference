# Verifalia: List User Certificates

Retrieves user certificates from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-user-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-user-certificates?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/list-user-certificates?${params}`, {
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
| `userId` | string | yes | The Verifalia user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "id": "string",
      "issuer": "string",
      "notAfter": "string",
      "notBefore": "string",
      "subject": "string",
      "thumbprint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string | When the certificate was uploaded to Verifalia. |
| `id` | string | The client certificate ID. |
| `issuer` | string | The certificate issuer. |
| `notAfter` | string | When the certificate expires. |
| `notBefore` | string | When the certificate becomes valid. |
| `subject` | string | The certificate subject. |
| `thumbprint` | string | The certificate thumbprint. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /users/{user-id}/certificates` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-certificates.md) for the provider-specific parameters and requirements.

