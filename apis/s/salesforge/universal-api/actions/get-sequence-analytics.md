# Salesforge: Get Sequence Analytics

Retrieves sequence analytics from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-analytics?connectionId=$CONNECTION_ID&workspaceID=wks_989gtkhm1ir6z8hdv3gjn&sequenceID=seq_q266pc1d33ozbe3et0mes&fromDate=2026-03-01&toDate=2026-03-25" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes",
  "fromDate": "2026-03-01",
  "toDate": "2026-03-25"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-analytics?${params}`, {
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
| `workspaceID` | string | yes | Workspace ID for the sequence. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceID` | string | yes | Sequence ID to analyze. Example: `seq_q266pc1d33ozbe3et0mes`. |
| `fromDate` | string | yes | Start date for analytics in YYYY-MM-DD format. Example: `2026-03-01`. |
| `toDate` | string | yes | End date for analytics in YYYY-MM-DD format. Example: `2026-03-25`. |
| `timezone` | string | no | Optional timezone for analytics aggregation. Example: `America/New_York`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/sequences/:sequenceID/analytics` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sequence-analytics.md) for the provider-specific parameters and requirements.

