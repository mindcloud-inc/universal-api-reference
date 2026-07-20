# iubenda: List Consents

Retrieves consents from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-consents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-consents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-consents?${params}`, {
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
| `subjectId` | string | no | Filter by subject ID. Example: `bd86b950-af4b-4a4f-9792-1690c18d42f1`. |
| `subjectEmailExact` | string | no | Filter by an exact subject email address. Example: `alex@example.com`. |
| `subjectFirstName` | string | no | Filter by an exact subject first name. Example: `Alex`. |
| `subjectLastName` | string | no | Filter by an exact subject last name. Example: `Morgan`. |
| `subjectVerified` | boolean | no | Filter by subject verified status. Example: `true`. |
| `source` | string | no | Filter by consent source: public or private. Example: `private`. |
| `ipAddress` | string | no | Filter by IP address. Example: `127.0.0.1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromTime` | string | no | Return consents from this timestamp onward. Example: `2026-03-01T00:00:00Z`. |
| `toTime` | string | no | Return consents up to this timestamp. Example: `2026-03-18T23:59:59Z`. |
| `startingAfter` | string | no | Cursor indicating after which consent results should be returned. Example: `last_consent_id`. |
| `limit` | number | no | Maximum number of consents to return. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "ip_address": "string",
      "owner": "string",
      "preferences": {},
      "source": "string",
      "subject": {},
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique consent identifier. |
| `ip_address` | string | IP address stored with the consent, if available. |
| `owner` | string | Identifier of the iubenda account owner. |
| `preferences` | object | Consent preferences keyed by preference name. |
| `source` | string | Whether the consent came from a public or private API key. |
| `subject` | object | Subject summary for the consent. |
| `timestamp` | string | Consent timestamp. |

## Native endpoint

Through the native iubenda API, this operation is `GET /consent` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-consents.md) for the provider-specific parameters and requirements.

