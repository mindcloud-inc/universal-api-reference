# Crossmint: Get Credential by Credential ID

Retrieves a credential from Crossmint by credential ID.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-credential-by-credential-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-credential-by-credential-id?connectionId=$CONNECTION_ID&id=urn%3Auuid%3Aff8be7d6-adc3-4524-b8ee-737564d31357" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "urn:uuid:ff8be7d6-adc3-4524-b8ee-737564d31357"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-credential-by-credential-id?${params}`, {
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
| `id` | string | yes | Credential identifier in `urn:uuid:<UUID>` format. Example: `urn:uuid:ff8be7d6-adc3-4524-b8ee-737564d31357`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "encryptedCredential": {},
      "unencryptedCredential": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `encryptedCredential` | object | Encrypted credential payload returned by Crossmint. |
| `unencryptedCredential` | object | Readable credential payload returned by Crossmint. |

## Native endpoint

Through the native Crossmint API, this operation is `GET /v1-alpha1/credentials/:id` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credential-by-credential-id.md) for the provider-specific parameters and requirements.

