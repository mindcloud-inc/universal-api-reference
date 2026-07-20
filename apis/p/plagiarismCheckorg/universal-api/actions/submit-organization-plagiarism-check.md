# PlagiarismCheck.org: Submit Organization Plagiarism Check



```
POST https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-organization-plagiarism-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-organization-plagiarism-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupToken": "string",
  "author": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-organization-plagiarism-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupToken": "string",
    "author": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupToken` | string | yes | Organization group token required for organization plagiarism checks. |
| `author` | string | yes | Email of the organization member who will own the check. |
| `text` | string | yes | Plain text content to check within the organization account. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PlagiarismCheck.org API returns.

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `POST /api/org/text/check/` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-organization-plagiarism-check.md) for the provider-specific parameters and requirements.

