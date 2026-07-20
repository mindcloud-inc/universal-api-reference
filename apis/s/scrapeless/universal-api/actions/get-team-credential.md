# Scrapeless: Get Team Credential

Retrieves a team credential from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-team-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-team-credential?connectionId=$CONNECTION_ID&origin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "origin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-team-credential?${params}`, {
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
| `origin` | string | yes | The origin URL (domain) for which credentials are stored |
| `namespace` | string | no | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
| `xApiToken` | string | no | API key for authentication |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "namespace": "Ava Chen",
      "origin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Credential metadata containing authentication data such as username, password, API keys, etc. |
| `namespace` | string | Optional namespace for credential organization (e.g., 'production', 'staging', 'development') |
| `origin` | string | The origin URL (domain) for which credentials are stored |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/credentials` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-credential.md) for the provider-specific parameters and requirements.

