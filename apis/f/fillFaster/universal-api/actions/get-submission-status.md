# FillFaster: Get Submission Status

Retrieves submission status from FillFaster by submission ID.

```
GET https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-submission-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-submission-status?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-submission-status?${params}`, {
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
| `submissionId` | string | yes | FillFaster submission identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": "string",
      "lastActionTimestamp": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "submissionFileLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | string | FillFaster form identifier. |
| `lastActionTimestamp` | date | Timestamp of the last recorded submission action. |
| `status` | string | Submission lifecycle status. |
| `submissionFileLink` | string | Public PDF file link when the submission is complete. |

## Native endpoint

Through the native FillFaster API, this operation is `GET /v1/getSubmissionStatus/:submissionId` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-status.md) for the provider-specific parameters and requirements.

