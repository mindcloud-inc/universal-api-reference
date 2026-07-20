# iubenda: Create Consent

Creates a consent in iubenda.

```
POST https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-consent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-consent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-consent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject.id` | string | no | Subject ID for the consent event. Example: `bd86b950-af4b-4a4f-9792-1690c18d42f1`. |
| `subject.email` | string | no | Subject email address for the consent event. Example: `alex@example.com`. |
| `subject.firstName` | string | no | Subject first name for the consent event. Example: `Alex`. |
| `subject.lastName` | string | no | Subject last name for the consent event. Example: `Morgan`. |
| `legalNotices[].identifier` | string | no | Identifier of a legal notice associated with the consent. Example: `codex_test_20260318_183536`. |
| `proofs[].content` | string | no | Proof content for the consent. Example: `Accepted privacy policy from signup form`. |
| `proofs[].form` | string | no | Proof form for the consent. Example: `Website signup form`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | object | no | Subject data for the consent event. |
| `subject.fullName` | string | no | Subject full name for the consent event. Example: `Alex Morgan`. |
| `subject.verified` | boolean | no | Whether the consent subject is verified. Example: `true`. |
| `subject.phones[]` | array<object> | no | Array of phone objects for the consent subject. |
| `subject.phones[].number` | string | no | A phone number with country code prefix for the consent subject. Example: `+5511999999999`. |
| `subject.phones[].label` | string | no | Label used to identify the consent subject phone number. Example: `personal`. |
| `legalNotices[]` | array<object> | no | Legal notices associated with the consent. |
| `legalNotices[].version` | string | no | Version of the associated legal notice. Auto-filled by iubenda when omitted. Example: `3`. |
| `proofs[]` | array<object> | no | Proof entries associated with the consent. |
| `proofDocumentIds[]` | array<string> | no | IDs of documents that provide proof of the consent. Example: `456f1ede-028c-4b96-b0bc-a8d2e85a975c`. |
| `preferences` | object | no | Consent preference values keyed by preference name. Example: `[object Object]`. |
| `ipAddress` | string | no | IP address associated with the consent event. Example: `127.0.0.1`. |
| `timestamp` | string | no | ISO 8601 timestamp at which the consent occurred. Example: `2026-03-18T21:37:27Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "subject_id": "string",
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
| `subject_id` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native iubenda API, this operation is `POST /consent` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-consent.md) for the provider-specific parameters and requirements.

