# Facebook: List Daily Ad Insights

Retrieves daily spend, clicks, and conversion events for Meta ads.

```
GET https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-daily-ad-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-daily-ad-insights?connectionId=$CONNECTION_ID&limit=25&offset=0&adAccountId=act_1234567890&endDate=YYYY-MM-DD&startDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "adAccountId": "act_1234567890",
  "endDate": "YYYY-MM-DD",
  "startDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-daily-ad-insights?${params}`, {
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
| `adAccountId` | string | yes | Enter the Meta ad account ID including the act_ prefix. Example: `act_1234567890`. |
| `endDate` | string | yes | Use YYYY-MM-DD. The date is included in the report. Example: `YYYY-MM-DD`. |
| `startDate` | string | yes | Use YYYY-MM-DD. The date is included in the report. Example: `YYYY-MM-DD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCurrency": "string",
      "actions": [
        {
          "actionType": "string",
          "value": "string"
        }
      ],
      "adId": "string",
      "adName": "Ava Chen",
      "clicks": "string",
      "dateStart": "string",
      "dateStop": "string",
      "spend": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCurrency` | string |  |
| `actions[].actionType` | string |  |
| `actions[].value` | string |  |
| `adId` | string |  |
| `adName` | string |  |
| `clicks` | string |  |
| `dateStart` | string |  |
| `dateStop` | string |  |
| `spend` | string |  |

## Native endpoint

Through the native Facebook API, this operation is `GET :adAccountId/insights` (base URL `https://graph.facebook.com/v25.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-daily-ad-insights.md) for the provider-specific parameters and requirements.

