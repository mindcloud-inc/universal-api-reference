# api.video: Get summary details

Retrieves summary source details from api.video.

```
GET https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/get-summary-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api.video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/get-summary-details?connectionId=$CONNECTION_ID&summaryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "summaryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/get-summary-details?${params}`, {
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
| `summaryId` | string | yes | The unique identifier for the summary. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native api.video API returns.

## Native endpoint

Through the native api.video API, this operation is `GET /summaries/:summaryId/source` (base URL `https://ws.api.video`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-summary-details.md) for the provider-specific parameters and requirements.

