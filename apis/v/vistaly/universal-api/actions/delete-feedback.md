# Vistaly: Delete Feedback

Deletes existing feedback from Vistaly.

```
DELETE https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/delete-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/delete-feedback?connectionId=$CONNECTION_ID&feedbackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedbackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/delete-feedback?${params}`, {
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
| `feedbackId` | string | yes | The unique identifier for the feedback. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vistaly API returns.

## Native endpoint

Through the native Vistaly API, this operation is `DELETE /v1/feedback/{feedbackId}` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-feedback.md) for the provider-specific parameters and requirements.

