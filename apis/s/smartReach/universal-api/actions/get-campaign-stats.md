# SmartReach: Get Campaign Stats

Retrieves campaign stats from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-campaign-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-campaign-stats?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-campaign-stats?${params}`, {
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
| `campaignId` | string | yes | ID of campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "object": "string",
      "total_opened": 1,
      "total_replied": 1,
      "total_sent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `object` | string |  |
| `total_opened` | number |  |
| `total_replied` | number |  |
| `total_sent` | number |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /campaigns/:campaign_id/stats` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-stats.md) for the provider-specific parameters and requirements.

