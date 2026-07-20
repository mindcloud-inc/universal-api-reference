# ZAP POST: Get Rejected Records For Submission

Retrieves rejected records for a specific submission from ZAP POST.

```
GET https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/get-rejected-records-for-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/get-rejected-records-for-submission?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/get-rejected-records-for-submission?${params}`, {
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
| `submissionId` | string | yes | The submission UUID to inspect rejected records for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "submissions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Campaign identifier for the rejected-record response. |
| `submissions` | object | Rejected-record payload grouped under submissions as returned by the API. |

## Native endpoint

Through the native ZAP POST API, this operation is `GET /api/v1/RejectedRecords/:submissionId` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rejected-records-for-submission.md) for the provider-specific parameters and requirements.

