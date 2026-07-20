# iubenda: Get Latest Consent for Subject

Retrieves the latest consent for a subject from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-latest-consent-for-subject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-latest-consent-for-subject?connectionId=$CONNECTION_ID&subjectId=bd86b950-af4b-4a4f-9792-1690c18d42f1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subjectId": "bd86b950-af4b-4a4f-9792-1690c18d42f1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-latest-consent-for-subject?${params}`, {
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
| `subjectId` | string | yes | Unique identifier of the subject whose latest consent should be returned Example: `bd86b950-af4b-4a4f-9792-1690c18d42f1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "ip_address": "string",
      "legal_notices": [
        {}
      ],
      "owner": "string",
      "preferences": {},
      "proof_documents": [
        "string"
      ],
      "proofs": [
        {}
      ],
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
| `id` | string |  |
| `ip_address` | string |  |
| `legal_notices` | array<object> |  |
| `owner` | string |  |
| `preferences` | object |  |
| `proof_documents` | array |  |
| `proofs` | array<object> |  |
| `source` | string |  |
| `subject` | object |  |
| `timestamp` | string |  |

## Native endpoint

Through the native iubenda API, this operation is `GET /beta/subjects/:id/consent/last` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-consent-for-subject.md) for the provider-specific parameters and requirements.

