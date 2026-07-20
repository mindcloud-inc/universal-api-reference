# iubenda: Get Legal Notice Version

Retrieves a legal notice version from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-legal-notice-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-legal-notice-version?connectionId=$CONNECTION_ID&identifier=codex_test_20260318_183536&version=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "codex_test_20260318_183536",
  "version": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-legal-notice-version?${params}`, {
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
| `identifier` | string | yes | Identifier of the legal notice Example: `codex_test_20260318_183536`. |
| `version` | number | yes | Version of the legal notice Example: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "documents": [
        {}
      ],
      "identifier": "string",
      "timestamp": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Legal notice content for the requested version. |
| `documents` | array<object> | Documents attached to this legal notice version. |
| `identifier` | string | Stable legal notice identifier. |
| `timestamp` | string | Legal notice version timestamp. |
| `version` | number | Legal notice version number. |

## Native endpoint

Through the native iubenda API, this operation is `GET /legal_notices/:identifier/:version` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-legal-notice-version.md) for the provider-specific parameters and requirements.

