# iubenda: List Legal Notice Versions

Retrieves legal notice versions from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-legal-notice-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-legal-notice-versions?connectionId=$CONNECTION_ID&identifier=privacy_policy_v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "privacy_policy_v1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-legal-notice-versions?${params}`, {
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
| `identifier` | string | yes | Identifier of the legal notice Example: `privacy_policy_v1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of legal notice versions to return. Example: `10`. |
| `startingAfter` | number | no | Cursor for pagination across legal notice versions. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `documents` | array<object> | Documents attached to this legal notice version. |
| `identifier` | string | Stable legal notice identifier. |
| `timestamp` | string | Legal notice version timestamp. |
| `version` | number | Legal notice version number. |

## Native endpoint

Through the native iubenda API, this operation is `GET /legal_notices/:identifier` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-legal-notice-versions.md) for the provider-specific parameters and requirements.

