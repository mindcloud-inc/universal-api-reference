# LaGrowthMachine: Get Campaign Stats

Retrieves campaign stats from LaGrowthMachine.

```
GET https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign-stats?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/get-campaign-stats?${params}`, {
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
| `campaignId` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceSize": 1,
      "campaignId": "string",
      "completed": 1,
      "converted": 1,
      "started": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceSize` | number | Campaign audience size. |
| `campaignId` | string | Campaign identifier. |
| `completed` | number | Completed lead count. |
| `converted` | number | Converted lead count. |
| `started` | number | Started lead count. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `GET /campaigns/:campaignId/stats` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-stats.md) for the provider-specific parameters and requirements.

