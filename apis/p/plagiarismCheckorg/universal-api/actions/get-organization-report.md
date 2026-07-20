# PlagiarismCheck.org: Get Organization Report



```
GET https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-organization-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-organization-report?connectionId=$CONNECTION_ID&id=1&groupToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "groupToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/get-organization-report?${params}`, {
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
| `id` | number | yes | Organization plagiarism check identifier. |
| `groupToken` | string | yes | Organization group token required for organization plagiarism checks. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PlagiarismCheck.org API returns.

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `POST /api/org/text/report/:id/` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-report.md) for the provider-specific parameters and requirements.

