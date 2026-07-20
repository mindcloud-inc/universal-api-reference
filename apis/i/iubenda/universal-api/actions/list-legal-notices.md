# iubenda: List Legal Notices

Retrieves legal notices from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-legal-notices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-legal-notices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-legal-notices?${params}`, {
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
| `identifier` | string | no | Filter by an exact legal notice identifier. Example: `privacy_policy_v1`. |
| `version` | number | no | Filter by an exact legal notice version. Example: `3`. |
| `language` | string | no | Filter legal notices by content language such as en or it. Example: `en`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `legalNoticeId` | string | no | Filter by an exact legal notice ID. Example: `0_privacy_policy`. |
| `fromTime` | string | no | Return legal notices from this timestamp onward. Example: `2026-03-01T00:00:00Z`. |
| `toTime` | string | no | Return legal notices up to this timestamp. Example: `2026-03-18T23:59:59Z`. |
| `startingAfterIdentifier` | string | no | Cursor identifier component for legal notice pagination. Example: `privacy_policy_v1`. |
| `startingAfterVersion` | number | no | Cursor version component for legal notice pagination. Example: `3`. |
| `limit` | number | no | Maximum number of legal notices to return. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "id": "string",
      "identifier": "string",
      "owner_id": "string",
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
| `content` | object | Legal notice content keyed by language code. |
| `id` | string | Unique legal notice identifier for this stored revision. |
| `identifier` | string | Stable legal notice identifier. |
| `owner_id` | string | Identifier of the iubenda account owner. |
| `timestamp` | string | Legal notice timestamp. |
| `version` | number | Legal notice version number. |

## Native endpoint

Through the native iubenda API, this operation is `GET /legal_notices` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-legal-notices.md) for the provider-specific parameters and requirements.

