# iubenda: Create Legal Notice

Creates a legal notice in iubenda.

```
POST https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-legal-notice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-legal-notice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "privacy_policy_v1",
  "content": "We collect your email address to send product updates."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-legal-notice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "privacy_policy_v1",
    "content": "We collect your email address to send product updates."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Stable legal notice identifier. Example: `privacy_policy_v1`. |
| `content` | string | yes | Legal notice content, as a string or language-keyed object. Example: `We collect your email address to send product updates.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timestamp` | string | no | Legal notice timestamp. Example: `2026-03-18T21:44:43Z`. |
| `documentIds[]` | array<string> | no | Document IDs associated with the legal notice. Example: `456f1ede-028c-4b96-b0bc-a8d2e85a975c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `identifier` | string |  |
| `timestamp` | string |  |
| `version` | number |  |

## Native endpoint

Through the native iubenda API, this operation is `POST /legal_notices` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-legal-notice.md) for the provider-specific parameters and requirements.

