# Diffbot: Retrieve Bulk Extract Job Data

Downloads extracted data for a Diffbot bulk extract job.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/retrieve-bulk-extract-job-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/retrieve-bulk-extract-job-data?connectionId=$CONNECTION_ID&jobName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/retrieve-bulk-extract-job-data?${params}`, {
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
| `jobName` | string | yes | Bulk extract job name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffbot API returns.

## Native endpoint

Through the native Diffbot API, this operation is `GET /v3/bulk/data` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bulk-extract-job-data.md) for the provider-specific parameters and requirements.

