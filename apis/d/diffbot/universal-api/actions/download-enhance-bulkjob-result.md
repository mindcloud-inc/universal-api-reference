# Diffbot: Download Enhance Bulkjob Result

Downloads a single result from a Diffbot Enhance bulk job.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/download-enhance-bulkjob-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/download-enhance-bulkjob-result?connectionId=$CONNECTION_ID&bulkjobId=string&jobIdx=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkjobId": "string",
  "jobIdx": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/download-enhance-bulkjob-result?${params}`, {
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
| `bulkjobId` | string | yes | Enhance bulkjob identifier. |
| `jobIdx` | string | yes | Result index inside the enhance bulkjob. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffbot API returns.

## Native endpoint

Through the native Diffbot API, this operation is `GET https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}/{jobIdx}` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-enhance-bulkjob-result.md) for the provider-specific parameters and requirements.

