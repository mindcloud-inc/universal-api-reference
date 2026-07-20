# CaptureIQ: Retrieve Recent Form Submission

Retrieves a recent form submission from CaptureIQ.

```
GET https://connect.mindcloud.co/v1/universal/captureIQ/latest/actions/retrieve-recent-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CaptureIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captureIQ/latest/actions/retrieve-recent-form-submission?connectionId=$CONNECTION_ID&workspaceId=68aec99d31016ef98d09fae3&formId=8feddac1-6f57-4c83-96ad-5767af6d2a4f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "68aec99d31016ef98d09fae3",
  "formId": "8feddac1-6f57-4c83-96ad-5767af6d2a4f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captureIQ/latest/actions/retrieve-recent-form-submission?${params}`, {
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
| `workspaceId` | string | yes | The ID of the workspace containing the form. Example: `68aec99d31016ef98d09fae3`. |
| `formId` | string | yes | The ID of the form to retrieve submissions from. Example: `8feddac1-6f57-4c83-96ad-5767af6d2a4f`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CaptureIQ API returns.

## Native endpoint

Through the native CaptureIQ API, this operation is `GET /ciq/recent-submission/v1` (base URL `https://www.app.captureiq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-recent-form-submission.md) for the provider-specific parameters and requirements.

