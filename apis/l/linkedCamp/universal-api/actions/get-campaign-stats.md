# LinkedCamp: Get Campaign Stats



```
GET https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-campaign-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-campaign-stats?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-campaign-stats?${params}`, {
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
| `campaignId` | string | yes | Campaign identifier. |
| `userId` | string | no | Optional user identifier for stats. |
| `range` | string | no | Optional date range for stats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted": 1,
      "campaignId": "string",
      "completed": 1,
      "engagements": 1,
      "failed": 1,
      "opportunities": 1,
      "processed": 1,
      "queue": 1,
      "replied": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted` | number | Accepted connection count. |
| `campaignId` | string | Campaign identifier. |
| `completed` | number | Completed record count. |
| `engagements` | number | Total campaign engagements. |
| `failed` | number | Failed record count. |
| `opportunities` | number | Opportunity count. |
| `processed` | number | Processed campaign records. |
| `queue` | number | Queued campaign records. |
| `replied` | number | Reply count. |
| `total` | number | Total leads or records counted for the campaign. |

## Native endpoint

Through the native LinkedCamp API, this operation is `GET /campaigns/:campaignId/stats` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-stats.md) for the provider-specific parameters and requirements.

