# SMSEdge: Get Sending Reports

Retrieves SMS sending reports from SMSEdge.

```
GET https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-sending-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSEdge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-sending-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-sending-reports?${params}`, {
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
| `date_from` | string | no | Filter results by minimum date in YYYY-MM-DD format. |
| `date_to` | string | no | Filter results by maximum date in YYYY-MM-DD format. |
| `limit` | number | no | Maximum items to return per request. |
| `offset` | number | no | Number of items to skip before returning results. |
| `status` | string | no | Filter by SMS sending status: sent, waiting, failed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSEdge API returns.

## Native endpoint

Through the native SMSEdge API, this operation is `GET /reports/sending/` (base URL `https://api.smsedge.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sending-reports.md) for the provider-specific parameters and requirements.

