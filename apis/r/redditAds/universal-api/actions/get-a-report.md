# Reddit Lead Ads: Get A Report

Generates a metrics report in Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-a-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-a-report?connectionId=$CONNECTION_ID&limit=25&offset=0&adAccountId=string&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "adAccountId": "string",
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-a-report?${params}`, {
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
| `adAccountId` | string | yes | The ID of the ad account to get the ads report under. |
| `data` | object | yes | JSON request body from the Reddit Ads API spec. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Report date. |
| `id` | string | Report identifier. |
| `name` | string | Report name. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `POST /ad_accounts/{ad_account_id}/reports` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-a-report.md) for the provider-specific parameters and requirements.

