# Verifalia: Upload User Certificate

Uploads a user certificate to Verifalia.

```
POST https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/upload-user-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/upload-user-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/upload-user-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native Verifalia API, this operation is `POST /users/{user-id}/certificates` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-user-certificate.md) for the provider-specific parameters and requirements.

