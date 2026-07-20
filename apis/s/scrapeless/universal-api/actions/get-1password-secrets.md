# Scrapeless: Get 1Password Secrets

Retrieves 1Password secrets from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-1password-secrets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-1password-secrets?connectionId=$CONNECTION_ID&references%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "references[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-1password-secrets?${params}`, {
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
| `xApiToken` | string | no | API key for authentication |
| `references[]` | array<string> | yes | Array of 1Password secret reference paths for batch retrieval of multiple secrets. Each reference format: `op://[vault]/[item]/[field]` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "secrets": {
        "error": "string",
        "reference": "string",
        "secret": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `secrets` | array<object> | List of secrets including both successfully retrieved secrets and error information for failed retrievals |
| `secrets.error` | string | Error message (if failed) |
| `secrets.reference` | string | The original reference path |
| `secrets.secret` | string | The secret value (if successful) |

## Native endpoint

Through the native Scrapeless API, this operation is `POST /browser/one-password/secrets` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-1password-secrets.md) for the provider-specific parameters and requirements.

