# Snapchat Ads: Get Ad Account Stats

Retrieves ad account performance stats from Snapchat Ads.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-ad-account-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-ad-account-stats?connectionId=$CONNECTION_ID&adAccountId=string&granularity=string&fields=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "granularity": "string",
  "fields": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-ad-account-stats?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID to report on. |
| `granularity` | string | yes | The reporting granularity, such as TOTAL, DAY, or HOUR. |
| `startTime` | date | no | The report start time in Snapchat's expected timestamp format. |
| `endTime` | date | no | The report end time in Snapchat's expected timestamp format. |
| `fields` | string | yes | Comma-separated Snapchat stats fields to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `breakdown` | string | no | Optional Snapchat stats breakdown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request_id": "string",
      "request_status": "string",
      "total_stats": {
        "impressions": 1,
        "spend": 1,
        "swipes": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_id` | string |  |
| `request_status` | string |  |
| `total_stats.impressions` | number |  |
| `total_stats.spend` | number |  |
| `total_stats.swipes` | number |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `GET /adaccounts/:adAccountId/stats` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ad-account-stats.md) for the provider-specific parameters and requirements.

