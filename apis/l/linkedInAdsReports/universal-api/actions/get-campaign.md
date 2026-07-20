# LinkedIn Ads Reports: Get Campaign

Retrieves a campaign from LinkedIn Ads Reports.

```
GET https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn Ads Reports `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-campaign?connectionId=$CONNECTION_ID&adAccountId=123456&campaignId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "123456",
  "campaignId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-campaign?${params}`, {
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
| `adAccountId` | string | yes | LinkedIn numeric ad account ID. Default: `123456`. |
| `campaignId` | string | yes | LinkedIn numeric sponsored campaign ID. Default: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignGroup": "string",
      "dailyBudget": {},
      "id": "string",
      "name": "Ava Chen",
      "runSchedule": {},
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignGroup` | string |  |
| `dailyBudget` | object |  |
| `id` | string |  |
| `name` | string |  |
| `runSchedule` | object |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LinkedIn Ads Reports API, this operation is `GET /rest/adAccounts/{{adAccountId}}/adCampaigns/{{campaignId}}` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

