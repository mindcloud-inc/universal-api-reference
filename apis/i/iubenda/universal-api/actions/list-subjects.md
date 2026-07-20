# iubenda: List Subjects

Retrieves subjects from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-subjects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-subjects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-subjects?${params}`, {
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
| `subjectId` | string | no | Filter by an exact subject ID. Example: `bd86b950-af4b-4a4f-9792-1690c18d42f1`. |
| `emailExact` | string | no | Filter by an exact subject email address. Example: `alex@example.com`. |
| `firstName` | string | no | Filter by an exact subject first name. Example: `Alex`. |
| `lastName` | string | no | Filter by an exact subject last name. Example: `Morgan`. |
| `verified` | boolean | no | Filter by verified status. Example: `true`. |
| `phone` | string | no | Filter subjects containing the given phone number with country code. Example: `+5511999999999`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromTime` | string | no | Return subjects from this timestamp onward. Example: `2026-03-01T00:00:00Z`. |
| `toTime` | string | no | Return subjects up to this timestamp. Example: `2026-03-18T23:59:59Z`. |
| `startingAfter` | string | no | Cursor indicating after which subject results should be returned. Example: `last_subject_id`. |
| `limit` | number | no | Maximum number of subjects to return. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "last_name": "Chen",
      "owner_id": "string",
      "preferences": {},
      "timestamp": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Subject email address. |
| `first_name` | string | Subject first name. |
| `full_name` | string | Subject full name. |
| `id` | string | Unique subject identifier. |
| `last_name` | string | Subject last name. |
| `owner_id` | string | Identifier of the iubenda account owner. |
| `preferences` | object | Subject preference summary, if present. |
| `timestamp` | string | Subject creation timestamp. |
| `verified` | boolean | Whether the subject is verified. |

## Native endpoint

Through the native iubenda API, this operation is `GET /subjects` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subjects.md) for the provider-specific parameters and requirements.

