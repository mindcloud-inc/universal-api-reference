# Peach: Get Campaign Stats

Retrieves campaign performance statistics from Peach.

```
GET https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-campaign-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-campaign-stats?connectionId=$CONNECTION_ID&accountId=string&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-campaign-stats?${params}`, {
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
| `accountId` | string | yes | The Peach account ID for the campaign owner. |
| `campaignId` | string | yes | The unique identifier of the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignGoal": 1,
      "campaignGroups": {},
      "totalDonationCount": 1,
      "totalSum": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignGoal` | number |  |
| `campaignGroups` | object | Map of campaign group ids to aggregate statistics. |
| `totalDonationCount` | number |  |
| `totalSum` | object |  |

## Native endpoint

Through the native Peach API, this operation is `GET /campaigns/stats/:accountId/:campaignId` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-stats.md) for the provider-specific parameters and requirements.

