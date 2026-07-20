# FillFaster: Create Bulk Submissions

Creates multiple submissions in FillFaster.

```
POST https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-bulk-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-bulk-submissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "submissions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-bulk-submissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "submissions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submissions[]` | array<object> | yes | Root array of bulk submission objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "status": 1,
      "submissionId": "string",
      "submissionLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Per-row error message when the row fails. |
| `status` | number | Per-row HTTP-style status code. |
| `submissionId` | string | Created FillFaster submission identifier when the row succeeds. |
| `submissionLink` | string | Generated FillFaster submission URL when the row succeeds. |

## Native endpoint

Through the native FillFaster API, this operation is `POST /v1/submission/createBulkSubmissions` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-submissions.md) for the provider-specific parameters and requirements.

