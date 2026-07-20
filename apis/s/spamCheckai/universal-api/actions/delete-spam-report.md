# SpamCheck.ai: Delete Spam Report

Deletes a spam report from SpamCheck.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/delete-spam-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpamCheck.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/delete-spam-report?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/delete-spam-report?${params}`, {
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
| `id` | number | yes | Spam report ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SpamCheck.ai API returns.

## Native endpoint

Through the native SpamCheck.ai API, this operation is `DELETE /spam_reports/:id` (base URL `https://api.spamcheck.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-spam-report.md) for the provider-specific parameters and requirements.

