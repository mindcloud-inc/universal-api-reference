# Crossmint: Verify Credential

Verifies a credential in Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/verify-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/verify-credential?connectionId=$CONNECTION_ID&credential=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credential": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/verify-credential?${params}`, {
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
| `credential` | object | yes | Credential object to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Verification error when the credential is invalid. |
| `isValid` | boolean | Whether Crossmint considers the credential valid. |

## Native endpoint

Through the native Crossmint API, this operation is `POST /v1-alpha1/credentials/verification/verify` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-credential.md) for the provider-specific parameters and requirements.

