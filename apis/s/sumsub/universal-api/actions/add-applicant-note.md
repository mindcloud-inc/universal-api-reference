# Sumsub: Add Applicant Note



```
POST https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/add-applicant-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/add-applicant-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicantId": "69e9345fee2635bd19c36a69",
  "note": "Disposable sandbox note from MindCloud Codex."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/add-applicant-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicantId": "69e9345fee2635bd19c36a69",
    "note": "Disposable sandbox note from MindCloud Codex."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applicantId` | string | yes | Unique Sumsub applicant identifier. Example: `69e9345fee2635bd19c36a69`. |
| `note` | string | yes | Text of the note to add to the applicant profile. Example: `Disposable sandbox note from MindCloud Codex.`. |
| `tags[]` | array<string> | no | Optional tags to associate with the note. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumsub API returns.

## Native endpoint

Through the native Sumsub API, this operation is `POST /resources/api/applicants/notes` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-applicant-note.md) for the provider-specific parameters and requirements.

