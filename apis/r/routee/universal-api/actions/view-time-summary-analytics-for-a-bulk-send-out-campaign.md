# Routee: View Time Summary Analytics for a bulk send out - campaign

Retrieves time summary analytics for a bulk send out - campaign from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-bulk-send-out-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-bulk-send-out-campaign?connectionId=$CONNECTION_ID&campaignId=string&offset=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "offset": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-bulk-send-out-campaign?${params}`, {
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
| `campaignId` | string | yes | The Id of the campaign |
| `offset` | date | yes | The time offset that the result will be calculated in ISO 8601. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `GET /reports/my/breakdown/perCampaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-time-summary-analytics-for-a-bulk-send-out-campaign.md) for the provider-specific parameters and requirements.

